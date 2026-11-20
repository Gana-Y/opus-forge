# Rename Map & Architectural Translation Ledger

This document is the **single source of truth** for all structural renames, command updates, and terminology translations across **OpusForge** (`opus-forge`).

## Translation Rules
1. **Functional Equivalence:** Every new term carries the exact functional, structural, and mathematical meaning of the original.
2. **Zero Brand Contamination:** All original repository titles, creator names, and trademarked skill phrases are replaced with native OpusForge terminology.
3. **Technical Invariance:** Standard technologies (CSS, ARIA, React, Next.js, Tailwind, Figma, MCP, framer-motion, HTML5, TypeScript) remain unmodified.
4. **Global Consistency:** Every occurrence across markdown files, JSON descriptors, frontmatter fields, code comments, and directory paths is updated identically.

| Original Name | New Name | Type | Semantic Justification |
|:---|:---|:---:|:---|
| `skills/` | `disciplines/` | Folder | Represents foundational craft disciplines rather than generic skill buckets |
| `emilkowalski-skills/` | `kinetic-physics/` | Folder | Focuses on fluid physics, spring curves, and direct manipulation |
| `impeccable/` | `structural-rigor/` | Folder | Focuses on UX topology, systematic layout, and defensive hardening |
| `taste-skill/` | `editorial-cadence/` | Folder | Focuses on spatial rhythm, high-conviction typography, and bespoke copy |
| `unslop/` | `aesthetic-sanitizer/` | Folder | Focuses on stripping out generic AI templates and visual cliches |
| `figma-mcp/` | `figma-conduit/` | Folder | Defines the live bridge for token extraction without copying Figma source |
| `master-skill` | `opus-pipeline` | Skill | The flagship end-to-end execution pipeline running all stages sequentially |
| `stage-1-figma` | `token-intake` | Stage | Extracts design variables, tokens, and frames via the Figma conduit |
| `stage-2-shape` | `blueprint` | Stage | Architects the UX flow, page mode, and structural wireframe |
| `stage-3-taste` | `editorial-craft` | Stage | Crafts layout hierarchy, bespoke copywriting, and hero moments |
| `stage-4-motion` | `kinetic-polish` | Stage | Applies interruptible spring physics and tactile feedback |
| `stage-5-harden` | `fortify` | Stage | Stress-tests edge cases, loading/error states, and WCAG accessibility |
| `stage-6-unslop` | `de-generic` | Stage | Sanitizes visual output to eliminate AI template signatures |
| `shape` | `blueprint` | Command / Skill | Architects information topology, viewport constraints, and user intent modes |
| `harden` | `fortify` | Command / Skill | Defensive interface engineering for boundary conditions and fault states |
| `critique` | `audit-rubric` | Command / File | Systematic evaluation against senior design engineering standards |
| `polish` | `micro-refine` | Command / File | Subtle alignment, token consistency, and visual balance sweeps |
| `delight` | `sensory-spark` | Command / File | Crafting memorable micro-delight moments and rewarding feedback |
| `bolder` | `amplify-weight` | Command / File | Enhances typographic hierarchy, contrast, and visual assertiveness |
| `quieter` | `subdue-presence` | Command / File | Restrains visual noise and reduces cognitive density |
| `distill` | `prune-density` | Command / File | Strips extraneous decorative elements to elevate core function |
| `clarify` | `demist-ui` | Command / File | Sharpens ambiguous labels, groupings, and interaction signifiers |
| `colorize` | `chroma-curate` | Command / File | Structures harmonious color ramps, contrast ratios, and semantic roles |
| `typeset` | `type-discipline` | Command / File | Enforces optical sizing, modular type scales, and line-height balance |
| `layout` | `spatial-cadence` | Command / File | Establishes geometric rhythm, margin consistency, and fluid breakpoints |
| `visualize` | `graphic-synthesize` | Command / File | Converts dense textual information into structured graphical schematics |
| `overdrive` | `hyper-impact` | Command / File | Unleashes high-energy creative flair for launch-grade landing pages |
| `extract` | `token-harvest` | Command / File | Mines design tokens, colors, and spatial units from existing codebases |
| `document` | `spec-generator` | Command / File | Compiles comprehensive DESIGN.md token ledgers and governance rules |
| `onboard` | `context-primer` | Command / File | Analyzes the existing repository environment to calibrate conventions |
| `adapt` | `viewport-conform` | Command / File | Translates interfaces across desktop, tablet, and mobile form factors |
| `mode-operate` | `mode-workspace` | Subfolder / Mode | Optimized ergonomics for data-dense productivity tools and dashboards |
| `mode-persuade` | `mode-editorial` | Subfolder / Mode | Narrative-driven visual persuasion for landing and marketing surfaces |
| `mode-read` | `mode-reading` | Subfolder / Mode | Distraction-free typographic layouts for long-form reading and documentation |
| `craft-floor.md` | `baseline-standards.md` | File | Defines the non-negotiable minimum threshold of UI quality |
| `foundations.md` | `core-axioms.md` | File | Core philosophical and architectural axioms of digital craftsmanship |
| `region-map.md` | `spatial-topology.md` | File | Maps interface zones, spatial hierarchies, and container bounds |
| `animate` | `motion-choreography` | Skill / Folder | End-to-end animation construction: triggers, properties, and exits |
| `animate-expo` | `mobile-physics-expo` | Skill / Folder | Native React Native and Expo spring gestures and haptic integration |
| `animation-performance` | `frame-budget-guard` | Skill / Folder | Preserving 60fps/120fps frame budgets and GPU composite layer audits |
| `animation-vocabulary` | `motion-lexicon` | Skill / Folder | Precision vocabulary mapping abstract visual ideas to exact physical terms |
| `apple-design` | `cupertino-physicality` | Skill / Folder | Fluid, continuous, and interruptible Apple HIG motion standards |
| `ask-emil` | `motion-advisor` | Skill / Folder | Consultative guidance for diagnosing stiff or artificial interface feel |
| `ask-sonner` | `toast-mechanics` | Skill / Folder | Non-blocking notification system physics, stacking, and dismissal |
| `break-ui` | `chaos-ui-tester` | Skill / Folder | Stress-testing layouts with extreme strings, broken data, and edge cases |
| `choreograph` | `orchestrate-sequences` | Skill / Folder | Coordinating multi-element staggered entrances and layout reflows |
| `emil-design-eng` | `tactile-craft-engineering` | Skill / Folder | Engineering tactile affordances, click depths, and micro-physics |
| `find-animation-opportunities` | `discover-motion-gaps` | Skill / Folder | Identifying static UI surfaces that demand physical feedback |
| `gestures` | `direct-manipulation` | Skill / Folder | 1:1 finger tracking, velocity inheritance, and momentum flings |
| `improve-animations` | `motion-overhaul` | Skill / Folder | Comprehensive audit and refactoring of lagging or mechanical transitions |
| `learn-taste` | `cultivate-aesthetic` | Skill / Folder | Developing discernment between cheap flashiness and enduring taste |
| `mobile-native` | `touch-fidelity` | Skill / Folder | Eliminating webview quirks to achieve authentic mobile application feel |
| `pick-ui-library` | `primitive-evaluator` | Skill / Folder | Objective evaluation of headless component libraries and motion runtimes |
| `prototype` | `rapid-harness` | Skill / Folder | Isolating experimental interactions in rapid throwaway testbeds |
| `remove-animations` | `motion-restraint` | Skill / Folder | Subtracting unnecessary, sluggish, or distracting visual motion |
| `review-animations` | `motion-critique` | Skill / Folder | Senior design engineering review of pull request motion diffs |
| `write-swift` | `swiftui-motion-patterns` | Skill / Folder | Idiomatic Swift 6 and SwiftUI gesture and animation architectures |
| `taste-skill` | `editorial-craft` | Skill / Folder | Anti-slop editorial design, rhythm, copywriting, and visual excellence |
| `references/backgrounds.md` | `references/backdrop-textures.md` | File | Subtle ambient gradients, grain, and high-end canvas treatments |
| `references/cards.md` | `references/surface-containers.md` | File | Container elevations, border luminance, and spatial card grouping |
| `references/copy.md` | `references/prose-architecture.md` | File | Writing distinctive, punchy, human copy with zero corporate jargon |
| `references/copy-moves.md` | `references/narrative-tactics.md` | File | Strategic rhetorical patterns that hook and convince visitors |
| `references/copy-registers.md` | `references/brand-tonalities.md` | File | Calibrating tonal voice between technical precision and emotional resonance |
| `references/copy-tells.md` | `references/cliche-indicators.md` | File | Detection catalogue for empty SaaS marketing fluff |
| `references/copy-voice.md` | `references/vocal-identity.md` | File | Formulating a memorable, consistent brand point-of-view |
| `references/diagrams.md` | `references/schematic-visuals.md` | File | Architectural visualizers that convey complex systems cleanly |
| `references/effects-creative.md` | `references/atmospheric-shaders.md` | File | High-performance WebGL and CSS shader atmospheres |
| `references/effects-objects.md` | `references/dimensional-objects.md` | File | Tactile 3D and faux-depth product representations |
| `references/effects-usage.md` | `references/fx-budget-rules.md` | File | Strict performance constraints governing graphic flourishes |
| `references/gate.md` | `references/finish-standards.md` | File | Rigorous pre-release checklist before code touches production |
| `references/icons.md` | `references/glyph-systems.md` | File | Cohesive iconography guidelines, line weights, and optical sizing |
| `references/layout-v4.md` | `references/viewport-geometry.md` | File | Screen-filling editorial viewport compositions and margin math |
| `references/moments.md` | `references/signature-interactions.md` | File | Defining 1-2 iconic interactive moments per page |
| `references/motion.md` | `references/spatial-kinetics.md` | File | Choreographing page transitions and scroll-driven revelations |
| `references/perf.md` | `references/render-budget.md` | File | Performance guardrails preventing asset-heavy page degradation |
| `references/photos.md` | `references/editorial-imagery.md` | File | Curation principles for authentic, non-stock photography |
| `references/scenes.md` | `references/environmental-stages.md` | File | Creating thematic scene-based backdrops for hero sections |
| `references/sections.md` | `references/view-segments.md` | File | Rhythmic distribution of page sections without visual monotony |
| `references/sections-library.md` | `references/section-catalog.md` | File | Curated patterns for headers, feature grids, and comparison tables |
| `references/system.md` | `references/foundational-tokens.md` | File | Unified spacing, typography, and color token architecture |
| `unslop` | `de-generic` | Skill / Folder | Purges generic AI hallmarks, clunky layouts, and cookie-cutter styles |
| `references/effects.md` | `references/filter-artifacts.md` | File | Eliminating overused glow effects, neon blobs, and purple blurs |
| `references/refs.md` | `references/anti-pattern-index.md` | File | Exhaustive index of common AI generator mistakes |
| `references/rtl.md` | `references/bidirectional-layout.md` | File | Ensuring faultless bidirectional and multilingual layout support |
| `references/signs.md` | `references/hallmark-smells.md` | File | Instant red flags that scream 'unmodified AI generation' |
| `references/tokens.md` | `references/sanitized-tokens.md` | File | Replacing random hex colors with coherent semantic design tokens |
| `references/visuals.md` | `references/aesthetic-remediation.md` | File | Step-by-step transformations from amateur AI to bespoke craft |
| `performance-cheatsheet.md` | `runtime-efficiency-cheatsheet.md` | File | Quick-reference memory, compositor, and frame rate budget rules |
| `ui-cheatsheet.md` | `tactile-ui-cheatsheet.md` | File | Quick-reference interaction mechanics, border radii, and optical offsets |
| `SKILLS-CATALOG.md` | `DISCIPLINES-CATALOG.md` | File | Individual component developer guide for standalone tool usage |
| `VERIFICATION-REPORT.md` | `AUDIT-AND-VERIFICATION.md` | File | Mandatory final audit report verifying 100% parity and zero legacy names |

---

## Frontmatter & Prompt Trigger Mapping

| Original Trigger / Prompt | New OpusForge Trigger / Prompt | Target Discipline |
|:---|:---|:---|
| `impeccable shape` | `opus-pipeline blueprint` or `/blueprint` | Information architecture & page mode |
| `taste-skill` | `opus-pipeline editorial-craft` or `/editorial-craft` | Page layout, copywriting, and typography |
| `emilkowalski/skills` | `opus-pipeline kinetic-polish` or `/kinetic-polish` | Gestures, springs, and tactile feedback |
| `impeccable harden` | `opus-pipeline fortify` or `/fortify` | Edge cases, fault states, and accessibility |
| `unslop` | `opus-pipeline de-generic` or `/de-generic` | Elimination of generic AI visual signatures |
| `master-build` | `opus-pipeline full-build` | Full end-to-end 6-stage autonomous build |
