---
name: opus-pipeline
description: "The sovereign 6-stage autonomous AI design engineering pipeline for building high-craft, million-dollar web interfaces. Executes gated sequential passes through Token Intake (Figma MCP) -> UX Blueprint & Mode Selection -> Editorial Layout & Copywriting -> Kinetic Motion Physics -> Defensive Fortification -> Aesthetic Sanitization. Trigger with: 'opus-pipeline full-build' or 'build a complete website using OpusForge'."
---

# OpusForge Sovereign Build Pipeline (`opus-pipeline`)

This is the flagship orchestrator of **OpusForge**. It unifies structural UX topology, editorial copywriting, fluid physics-based motion, defensive resilience hardening, and anti-template aesthetic sanitization into a single sequential, gated execution engine.

```
┌────────────────────────────────────────────────────────────────────────┐
│                   OPUSFORGE SOVEREIGN PIPELINE                         │
├───────────────┬────────────────────────────────────────────────────────┤
│ Stage 1       │ TOKEN INTAKE: Figma MCP Inspection & Variable Harvest  │
│ Gate 1        │ Token Parity & Semantic Binding Verified               │
├───────────────┼────────────────────────────────────────────────────────┤
│ Stage 2       │ UX BLUEPRINT: Mode Selection, Hierarchy & Viewport Math│
│ Gate 2        │ Information Architecture & Mode Approved               │
├───────────────┼────────────────────────────────────────────────────────┤
│ Stage 3       │ EDITORIAL CRAFT: Section Rhythm & Bespoke Copywriting  │
│ Gate 3        │ Zero-Fluff Copy & Section Cadence Verified             │
├───────────────┼────────────────────────────────────────────────────────┤
│ Stage 4       │ KINETIC POLISH: Spring Physics, Gestures & Tactile Feel│
│ Gate 4        │ 60fps/120fps Composite Frame Budget Passed             │
├───────────────┼────────────────────────────────────────────────────────┤
│ Stage 5       │ DEFENSIVE FORTIFICATION: Fault Boundaries & WCAG A11y  │
│ Gate 5        │ Edge Cases, Empty States & Tab Traversal Verified      │
├───────────────┼────────────────────────────────────────────────────────┤
│ Stage 6       │ AESTHETIC SANITIZATION: De-Generic De-Templating Pass  │
│ Gate 6        │ Zero AI Slop Signatures (No Glow Blobs, Real Craft)    │
└───────────────┴────────────────────────────────────────────────────────┘
```

---

## The Non-Negotiable Operational Rules

1. **Strict Sequential Progression:** You must execute Stages 1 through 6 in exact order. Never skip a stage, never merge stages, and never proceed past a gate without generating an explicit verification report with file/line evidence.
2. **Pre-Flight Task Checklist:** Before writing a single line of code, emit a comprehensive numbered checklist spanning every deliverable across all 6 stages.
3. **Evidence-Based Gating:** At the conclusion of each stage, output a stage completion report citing concrete evidence (file paths, CSS token bindings, component names, or test outputs).
4. **Anti-Skipping Protocol:** If any stage encounters a missing asset or blocked dependency, stop, report the exact block to the user, and resolve it before proceeding. Never silently improvise around missing requirements.
5. **Final Comprehensive Audit:** Upon completing Stage 6, re-crawl the pre-flight checklist end-to-end. If any requirement lacks proof-of-work, immediately implement and verify it.

---

## Master Execution Stages

### Stage 1: Design Intake & Token Harvest (`token-intake`)
*Sub-discipline reference: `disciplines/figma-conduit/SETUP.md`*

- **Trigger:** Check for a provided Figma URL or design specification.
- **Actions:**
  1. If a Figma URL is provided: invoke `get_design_context` targeting key frames and `get_motion_context` for prototype curves.
  2. If building from a written brief: calibrate project context via `disciplines/structural-rigor/reference/context-primer.md`.
  3. Extract core design tokens into `tokens.css`:
     - Spacing scale (`--space-1` through `--space-16`).
     - Neutral palette with tonal tinting (`--canvas-bg`, `--surface-card`, `--border-subtle`).
     - Accent chromatic token (`--accent-primary`, `--accent-hover`).
     - Typographic scale and font pairings (`--font-display`, `--font-body`, `--font-mono`).
- **Gate 1 Criteria:** Design tokens are declared in CSS variables and verified against Figma specs or brief requirements.

---

### Stage 2: UX Architecture & Mode Blueprinting (`blueprint`)
*Sub-discipline reference: `disciplines/structural-rigor/reference/blueprint.md`*

- **Intent:** Define what visitor success looks like on this surface and establish spatial hierarchy.
- **Actions:**
  1. Select the primary surface mode:
     - **Persuade (Editorial):** Visitor acts/converts; high expression, bold hero, bespoke world.
     - **Workspace (Operate):** Visitor accomplishes tasks; high scanability, dense utility, calm chrome.
     - **Reading (Read):** Visitor comprehends documentation; disciplined type, optimal line length (65ch).
  2. Map spatial zones per `disciplines/structural-rigor/reference/spatial-topology.md`:
     - Header navigation and persistent anchors.
     - Focal hero container.
     - Feature topology and comparison matrices.
     - Global footer and legal/attribution anchor.
  3. Establish container constraints: equal left and right margins, max-content bounds, and responsive fluid breakpoints (390px, 768px, 1024px, 1440px).
- **Gate 2 Criteria:** Information architecture, route hierarchy, and surface mode are documented and locked.

---

### Stage 3: Editorial Layout & Copywriting (`editorial-craft`)
*Sub-discipline reference: `disciplines/editorial-cadence/editorial-craft/SKILL.md`*

- **Intent:** Write human, punchy, non-corporate copy and enforce "one section per screen" visual rhythm.
- **Actions:**
  1. Apply the 9 non-negotiable house rules from `editorial-craft`:
     - **Rule 1:** Zero captions under images or visual renders; credits live exclusively in the footer.
     - **Rule 2:** Every visual renders; zero empty grounds or broken layout boxes at any viewport.
     - **Rule 3:** **One section per screen.** The hero alone occupies the first viewport (1440x900). Every subsequent section spans exactly 1 or 2 viewports tall. No section heading peeking over the fold.
     - **Rule 4:** Equal left and right content margins.
  2. Copywriting Architecture (`references/prose-architecture.md`):
     - Strip all corporate fluff: no "supercharge", "seamless", "next-gen", "all-in-one", or "revolutionize".
     - State plainly and specifically what is built, how it works, and why it matters.
     - Headlines are declarative, short, and carry an unmistakable brand perspective.
  3. Signature Moments (`references/signature-interactions.md`):
     - Craft 1–2 memorable, dealt interaction moments (e.g., an interactive interactive calculator, a physics dropzone, a scrubbable telemetry visualizer).
- **Gate 3 Criteria:** Layout satisfies the one-section-per-screen rhythm, copy is free of AI fluff, and the signature interactive moment is implemented.

---

### Stage 4: Kinetic Motion & Micro-Interactions (`kinetic-polish`)
*Sub-discipline reference: `disciplines/kinetic-physics/`*

- **Intent:** Implement living, tactile, physics-based motion with 60fps/120fps compositor guarantees.
- **Actions:**
  1. Apply decision hierarchy from `motion-choreography`:
     - Verify motion belongs: never animate keyboard actions, high-frequency data tables, or functional icons without purpose.
     - Never use raw `ease-in` for entrances; use authentic spring dynamics or snappy decelerations (`cubic-bezier(0.16, 1, 0.3, 1)`).
  2. Tactile Button & Modal Mechanics (`tactile-craft-engineering`):
     - Active press feedback: subtle scale (`0.98` to `0.99`) with instant onset and dampened release.
     - Modal backdrops: instantaneous composite opacity fades with subtle 10px Y-axis translation.
     - Toast notifications: non-blocking physics with swipe-to-dismiss momentum (`toast-mechanics`).
  3. Compositor Layer Budget (`frame-budget-guard`):
     - Animate strictly composite-only properties: `transform` and `opacity`.
     - Zero transitions on `height`, `width`, `margin`, or `top`/`left`.
  4. Accessibility: Mandatory `@media (prefers-reduced-motion: reduce)` override disabling all translational movement.
- **Gate 4 Criteria:** Transitions run purely on GPU composite layers, press states provide tactile click depth, and reduced-motion overrides are active.

---

### Stage 5: Defensive Fortification (`fortify`)
*Sub-discipline reference: `disciplines/structural-rigor/reference/fortify.md`*

- **Intent:** Battle-test the interface against extreme data, network anomalies, and accessibility barriers.
- **Actions:**
  1. Run the Chaos Test Suite (`disciplines/kinetic-physics/chaos-ui-tester`):
     - Zero items: clean, purposeful empty states with clear recovery actions.
     - Extreme data: test strings of 200+ characters, non-Latin scripts, unbreakable email strings, and massive numerical counts.
     - Boundary values: check 0, 1, 999999+ formatting and truncate with optical tooltips where appropriate.
  2. Network & Fault States:
     - Skeleton loaders matching the exact geometric footprint of loaded content (zero layout shift / CLS = 0).
     - Inline retry handlers and descriptive, actionable error notices.
  3. Accessibility & Keyboard Navigation (WCAG 2.1 AA):
     - Visible, high-contrast focus rings (`:focus-visible`).
     - Logical tab index flow across interactive controls.
     - Semantic ARIA roles (`role="dialog"`, `aria-expanded`, `aria-live="polite"`).
- **Gate 5 Criteria:** Zero overflow breaks under extreme strings, all interactive elements are 100% keyboard navigable, and empty/error states are functional.

---

### Stage 6: Aesthetic Sanitization Pass (`de-generic`)
*Sub-discipline reference: `disciplines/aesthetic-sanitizer/de-generic/SKILL.md`*

- **Intent:** Purge any residual synthetic AI tells, amateur styling, or cookie-cutter templates.
- **Actions:**
  1. Scan for Hallmark AI Smells (`references/hallmark-smells.md`):
     - ❌ Purple/violet gradient overlays and neon mesh halos.
     - ❌ Blurry glassmorphism cards with illegible text.
     - ❌ Random floating emoji badges ("New ✨", "AI-Powered 🚀").
     - ❌ Centered generic three-column feature cards with duplicate icons.
     - ❌ Gratuitous pulse animations on static buttons.
  2. Apply Craft Corrections (`references/aesthetic-remediation.md`):
     - Replace purple gradients with tinted ambient backdrops or clean physical lighting.
     - Flatten glassmorphic blur to crisp solid surfaces with 1px border luminance.
     - Ensure all feature cards have unique structural geometry and authentic telemetry data.
  3. Final Polish Pass (`disciplines/structural-rigor/reference/micro-refine.md`):
     - Optical alignment check on icons, labels, and badges.
     - Harmonize border-radii across nesting tiers (child radius = parent radius minus padding).
- **Gate 6 Criteria:** The interface looks bespoke, handcrafted by a senior design director, with zero generic AI styling tells.

---

## Final Verification Checklist

Prior to project handoff, the agent must execute the following automated audit:
```text
[ ] Stage 1: Tokens bound semantically in tokens.css (0 hardcoded hex/px in components).
[ ] Stage 2: Page mode declared; viewport boundaries and container geometry verified.
[ ] Stage 3: Section cadence verified (one section per screen at 1440x900); copy contains 0 marketing fluff words.
[ ] Stage 4: Transitions restricted to transform/opacity; spring curves applied; prefers-reduced-motion respected.
[ ] Stage 5: Empty, loading, and error states rendered; keyboard tab navigation tested; no text clipping on long strings.
[ ] Stage 6: 0 AI gradient halos, 0 emoji badges, 0 generic three-box cards; optical hierarchy locked.
```
