# /structural-rigor hooks

Manage the **design detector hook** for the current project.

The hook runs the structural-rigor design detector on direct file edits to design-relevant files (`.tsx`, `.jsx`, `.html`, `.vue`, `.svelte`, `.astro`, `.css`, `.scss`, `.sass`, `.less`, and plain `.ts` and `.js` in a project with a PRODUCT.md, DESIGN.md or `.structural-rigor` folder). Claude Code, Codex, Cursor, and GitHub Copilot use a post-tool-use hook and push a short system reminder into the agent's context after the edit; findings get a correction prompt, pending issues get a re-nudge, and clean UI-ish files get a short ack unless quiet mode is on (`hook.quiet` in config). Plain `.ts` and `.js` files are still scanned, but stay quiet unless the detector finds something. Grok Build fires the same PostToolUse scan to mark touched files, then surfaces findings on Stop `additionalContext`. Do not expect a Grok per-edit reminder: Grok discards that stdout. On Hermes Agent the per-edit findings arrive inside the `write_file` or `patch` tool result itself, as its `structural-rigor` field.

The detector rules run in two tiers. The per-edit hook surfaces only the immediate tier: mechanical, unambiguous problems worth interrupting an edit for, such as broken images, overflowing content, contrast and legibility failures, gradient text, glow shadows, and design-system drift. Everything else (copy cadence, palette and typography taste, layout rhythm) is deferred to a deep pass on the `Stop` hook event, which runs the full rule set over every UI file touched in the session and surfaces the remaining findings once, deduplicated against what the per-edit pass already reported. A session with nothing left to report stops silently. Set `hook.perEditRules` to `"all"` in `.structural-rigor/config.json` to restore the full rule set on every edit. The Stop deep pass is wired for Claude Code, Codex, and Grok Build, which dispatch a native `Stop` hook event, and for Hermes Agent, whose plugin sends it from `pre_verify`. Cursor does not get one (its `stop` hook can only answer with a follow-up user message), and GitHub Copilot's stop-style events do not feed context back to the model, so they keep the full detector per edit. Grok also fires an observe-only Stop with `reason: "shutdown"` after `end_turn`; skip that one, scan only `end_turn`.

Every hook is a mechanical pass. The reflexes no scanner catches live in [baseline-standards.md](baseline-standards.md), which the skill loads before it edits UI, so they apply whether or not a hook is wired. A session with no automatic hook gets one `MANUAL_DETECTOR_REQUIRED` directive from `structural-rigor context` asking for a single detector run at the end.

This command toggles the hook **per project** by editing `.structural-rigor/config.json` (the unified OpusForge Structural Rigor config; hook runtime settings live under its `hook` key, and shared detector ignores live under `detector`). Per-developer overrides, including the install consent decision (`hook.consent`) the CLI records, live in the gitignored `.structural-rigor/config.local.json`. Set `hook.enabled: false` to turn the hook off, `hook.quiet: true` to silence the clean/pending acks, or `hook.auditLog` to a file path for an NDJSON log. The legacy `IMPECCABLE_HOOK_DISABLED`, `IMPECCABLE_HOOK_QUIET`, and `IMPECCABLE_HOOK_LOG` env vars are still honored and override these config values when set.

Declare server-side template extensions under **`detector.extensions`** when the project uses Blade, Twig, ERB, or Handlebars files; the hook skips them otherwise because they sit outside the built-in extension list. One entry per extension, `{ "ext": ".blade.php", "engine": "html" }`. `engine` picks the analyzer (`html` for markup templates, `text` for JS/TS/CSS-like files) and defaults to `html`. Match against the end of the filename, so double extensions like `.blade.php` and `.html.erb` work. Config only adds extensions; the built-in list always applies.

Manual `{{scripts_path}}/structural-rigor detect` scans use the same project filter config by default: `detector.ignoreRules`, `detector.ignoreFiles`, `detector.ignoreValues`, and `detector.designSystem.enabled`. `hook.enabled` only controls automatic hook execution, not manual CLI scans. Use `{{scripts_path}}/structural-rigor detect --no-config ...` for a raw detector run that ignores project config/context. Use `{{scripts_path}}/structural-rigor ignores ...` for direct CLI CRUD on the same detector ignores.

Supported harnesses: Claude Code (`.claude/settings.local.json` for a project-scope install; `$CLAUDE_CONFIG_DIR/settings.json` for a user-scope install, defaulting to `~/.claude/settings.json`; a project hook moved into shared `.claude/settings.json` is honored in place too), Codex (`.codex/hooks.json` in the project; `$CODEX_HOME/hooks.json`, default `~/.codex/hooks.json`, for a user-scope install), Cursor (`.cursor/hooks.json` in the project; `~/.cursor/hooks.json` for a user-scope install), Grok Build (`.grok/hooks/structural-rigor.json` in the project, which requires `/hooks-trust` or `--trust`; the personal `~/.grok/hooks/structural-rigor.json` for a user-scope install), GitHub Copilot (`.github/hooks/structural-rigor.json` in the project, a team-shared committed file that both the Copilot CLI and the cloud agent read), and Hermes Agent (the `structural-rigor-design-hook` plugin in `~/.hermes/plugins/`; the user enables it once with `hermes plugins enable structural-rigor-design-hook`; a project install's launcher runs only in a project Hermes trusts, via `hermes skills trust`). For the Copilot CLI, repo-level hooks fire once `.github/hooks/structural-rigor.json` is committed to the repository's default branch.

On **Cursor**, the hook runs on `postToolUse` for the `Write` tool (every agent file edit) and returns its reminder as `additional_context`, which Cursor adds after the tool result. Projects set up before this ran a `preToolUse` gate (`hook-before-edit`) that blocked bad writes before they landed; that gate still works until `hooks on`, `structural-rigor update`, or `structural-rigor doctor --fix` moves the entry to `postToolUse`.

Gemini installs session and completion hooks in `.gemini/settings.json`, merged into the settings already there (comments are tolerated; a commented file is backed up to `settings.json.bak` before the rewrite, and a file that is not valid JSON is left alone). It does not install a per-edit detector hook. The `BeforeTool` hook only rewrites shell commands that run `build-phase`, and only on macOS and Linux; on Windows (where Gemini runs hooks through PowerShell) no session id reaches the shell, so a comp build is not tied to the session and the completion reminder stays silent.

When there is no project Claude skill, `hooks on` looks for `skills/structural-rigor/scripts/structural-rigor` inside `CLAUDE_CONFIG_DIR` (default `~/.claude`) and writes the hook into that account's `settings.json`, using the installed launcher's absolute path. Relative account directories resolve against the caller's working directory. An explicit account directory is exclusive: another account's default skill and settings are never substituted. Status and context read the same account settings. If no design harness can be wired, `hooks on` says so, reports skipped invalid settings or the missing skill lookup paths, and gives the next step.

Status checks the current event entries and matchers in each manifest, including the Stop pass where supported. Claude Code counts as wired when either project settings file (or its user settings file) contains the current entries. A legacy command, partial manifest, or missing file is reported as not wired. If enabled in config but no design harness is wired, status says so and gives `structural-rigor hooks on` as the repair command. An installed and enabled Hermes design-hook plugin also counts as wired; `on` acknowledges it without changing the plugin configuration. Wiring confirms the manifest entries; harness trust requirements and session reloads still apply.

When `hook.consent` is `"accepted"` in the project's `config.local.json` and the hook is enabled, `structural-rigor context` restores missing or stale entries for installed harness skills and reports repairs in one line. Shared config consent does not authorize this write. Automatic repair preserves unrelated settings and hooks and leaves malformed manifests alone. Without local consent, context writes no manifests and keeps `MANUAL_DETECTOR_REQUIRED`, naming the missing or stale harness wiring. Explicitly disabled hooks stay disabled.

## Routing

The first argument is the action. Defaults to `status`.

| Action | What it does |
|---|---|
| `status` | Print current state, shared/local config paths, ignored rules / files / values, env override, and actual manifest wiring for each harness. |
| `on` | Set `enabled: true` in `.structural-rigor/config.json`, record local hook consent as accepted, and install/repair provider hook manifests when the skill is installed. |
| `off` | Set `enabled: false` in `.structural-rigor/config.json`. |
| `ignore-rule <id>` | Append `<id>` to `detector.ignoreRules`; for `overused-font`, requires `--all-values`. Suppresses the rule across the whole project. |
| `ignore-file <glob>` | Append `<glob>` to `detector.ignoreFiles`. Suppresses **every** rule for matching files. |
| `ignore-value <id> <value> [--shared] [--reason "..."]` | Append a rule/value suppression to shared `.structural-rigor/config.json`. |
| `ignore-value <id> <value> --local [--reason "..."]` | Append a private rule/value suppression to `.structural-rigor/config.local.json`. |
| `ignore-value <id> "*" --file <glob> [--file <glob>...]` | Turn one rule off in matching files only, leaving it active everywhere else. Repeat `--file`, or use `--file=<glob>` / `--files=<glob>`. A bare `"*"` with no `--file` is refused: use `ignore-rule <id>` if you really mean project-wide. |
| `reset` | Delete the project config, dedup cache, and Cursor pending queue, and remove the hook's entries from every provider manifest `on` installs, the committed Copilot file included (a team-shared `settings.json` that `on` never writes is never touched). |

## Flow

1. Resolve the action from the user's argument. If no action was given, default to `status`.
2. Invoke the admin script and pass the user's output through verbatim:

   ```bash
   {{scripts_path}}/structural-rigor hooks <action> [args...]
   ```

3. If `<action>` is `off`, follow up with a one-line note: "Done. New edits will not trigger the design hook in this project until you run `{{command_prefix}}structural-rigor hooks on`."
4. If `<action>` is `on`, report what the command installed or repaired. If no installed skill folders were found or settings were skipped, surface that result and do not claim the hook will run. Otherwise note that the harness must load the updated settings (and satisfy any trust requirements) before it runs. On Hermes Agent, `on` cannot install or enable the plugin: if `structural-rigor context` reported `MANUAL_DETECTOR_REQUIRED`, tell the user to run `npx structural-rigor install` and then `hermes plugins enable structural-rigor-design-hook` instead.
5. If `<action>` is `ignore-value`, `ignore-file`, or `ignore-rule`, just print the script output. The default scope is shared `.structural-rigor/config.json`; add `--local` only when the user explicitly asks for a private exception.
6. If `<action>` is `status`, just print the script output. Do not add commentary unless the user asked a follow-up question.

## Triage findings

The hook itself never writes ignore config; every exception goes through `structural-rigor hooks`. Triage each finding into one of three outcomes:

- **Real design problem**: fix it. Never add an ignore to skip a fix or to push a blocked write through.
- **Confident false positive or sanctioned exception**: persist the narrowest ignore yourself and disclose it in your reply. The bar is evidence you can name: an intentional demo or fixture, documentation of bad design, literal or domain-appropriate motion (a ball that bounces), or a choice the user already confirmed. Put that evidence in `--reason` as `"<who decided: evidence>"`; write "user confirmed" only when the user actually did.
- **Unsure**: leave the finding standing and give the reason in one line. Ask the user only when you genuinely cannot decide.

Self-serve stops at `ignore-value`. `ignore-file` and `ignore-rule` silence too much to add on your own judgment; ask the user first.

Prefer the narrowest exception:

- If the finding line shows an `ignore-value <rule> <value>` pair, pass it to `structural-rigor hooks ignore-value` with your `--reason`. This writes shared `.structural-rigor/config.json` by default.
- For value-specific findings such as `overused-font` and `bounce-easing`, use `ignore-value` for the specific value. Do not use `ignore-rule overused-font` for a specific font.
- If the finding has no value-specific command, such as `side-tab`, scope that one rule to the file: `ignore-value <id> "*" --file <path>`. Run `{{scripts_path}}/structural-rigor detect <path>` first to see what actually fires there.
- Reach for `ignore-file <path>` only when the whole file is out of scope for design review: a fixture, a generated artifact, a deliberate slop demo. It silences every rule for that file permanently, including rules that have not been written yet. A real UI surface with one noisy rule wants the file-scoped value ignore above.
- Use `ignore-rule <id>` only when the user asks to suppress that whole rule across the project. For broad overused-font suppression, use `ignore-rule overused-font --all-values` only when the user asks to ignore overused fonts generally.
- Prefer config ignores (the commands above) by default; they keep suppressions in one reviewable place. Reach for an inline comment only when the waiver must travel with a single file that leaves the repo (a generated/exported standalone document, an emailed HTML file). The supported marker is `structural-rigor-disable <rule>` (whole file) or `structural-rigor-disable-line` / `structural-rigor-disable-next-line` (one line), in any comment syntax, with an optional reason after `:` or `--`. The detector honors it by default; `--no-inline-ignores` or `--no-config` bypasses it.

Example value-specific exception:

```bash
{{scripts_path}}/structural-rigor hooks ignore-value overused-font Inter --shared --reason "User confirmed Inter is intentional"
```

Example self-served exception, with the evidence named:

```bash
{{scripts_path}}/structural-rigor hooks ignore-value bounce-easing bounce-ball --shared --reason "Agent: literal ball-bounce animation, bounce easing is the subject"
```

Example whole-rule font exception:

```bash
{{scripts_path}}/structural-rigor hooks ignore-rule overused-font --all-values --reason "User asked to ignore overused fonts generally"
```

Example one-rule-in-one-file exception, for a file that is still worth reviewing
for everything else:

```bash
{{scripts_path}}/structural-rigor hooks ignore-value design-system-font-size "*" --file "src/overlay/widget.js" --reason "Injected widget builds its own type scale; DESIGN.md's ramp describes the site"
```

Example whole-file exception, for a file that is out of scope entirely:

```bash
{{scripts_path}}/structural-rigor hooks ignore-file "src/legacy/Card.tsx"
```

## Constraints

- Never modify `.structural-rigor/config.json` or `.structural-rigor/config.local.json` by hand from this command. Always go through `structural-rigor hooks` so writes stay validated and the file shape stays consistent. One exception: `detector.extensions` has no admin action, so when the user asks to cover a template stack, edit that one field in `.structural-rigor/config.json` directly and leave the rest of the file untouched.
- Do not edit the launcher or the binary behind `structural-rigor hook` and `structural-rigor hook-before-edit` from this flow. Those are skill plumbing.
- When a user asks how far to trust the hook, say it runs the engine unsandboxed with the agent's environment and network access (in the Copilot cloud agent too, once `.github/hooks/structural-rigor.json` is committed), and that the launcher checks a downloaded engine against `{{scripts_path}}/engine-checksums.txt` before its first run; **never** call it sandboxed.
- The hook never blocks an edit; it emits a post-edit reminder. (A Cursor project still on the old `preToolUse` gate can block a write until its manifest is migrated.) Disabling stops the reminders.
- The hook is bundled with the OpusForge Structural Rigor skill. Project installs use `.claude/settings.local.json`, `.codex/hooks.json`, `.cursor/hooks.json`, `.github/hooks/structural-rigor.json`, and `.gemini/settings.json`; a user-scope Claude install uses the active account's `$CLAUDE_CONFIG_DIR/settings.json` (default `~/.claude/settings.json`), and a user-scope Codex, Cursor or Grok install uses `~/.codex/hooks.json`, `~/.cursor/hooks.json` or `~/.grok/hooks/structural-rigor.json`. On Codex, the user must approve the hook via `/hooks` the first time. On Cursor, confirm hooks are enabled under Settings -> Hooks. On GitHub Copilot, the CLI loads `.github/hooks/structural-rigor.json` once it is committed to the repository's default branch, and the cloud agent reads it from the repo directly.

## Failure modes

- If `.structural-rigor/config.json` or `.structural-rigor/config.local.json` is unreadable or malformed, the hook ignores that file and uses the remaining valid config/defaults. `structural-rigor hooks status` will show malformed files as ignored.
- If the user asks to "disable the hook" globally, lead with `{{command_prefix}}structural-rigor hooks off` (persistent for this project; writes `hook.enabled: false` to config). The legacy `IMPECCABLE_HOOK_DISABLED=1` env var also works as a one-shot override that follows the shell.
