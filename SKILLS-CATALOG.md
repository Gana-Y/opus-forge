# OpusForge Disciplines & Skills Catalog (`DISCIPLINES-CATALOG.md`)

This is the **complete, exhaustive directory** of every individual discipline and capability in OpusForge. 

When you don't want to run the full 6-stage master pipeline (`opus-pipeline`), you can use this catalog to invoke **any single skill for an individual component, page, or interaction**.

---

## Quick Navigation
1. [Inspect & Token Harvesting](#1-inspect--token-harvesting)
2. [Kinetic Motion Physics (All 20 Skills)](#2-kinetic-motion-physics-all-20-skills)
3. [Structural Rigor & UX Architecture](#3-structural-rigor--ux-architecture)
4. [Editorial Cadence & Layout Rhythm](#4-editorial-cadence--layout-rhythm)
5. [Defensive Fortification](#5-defensive-fortification)
6. [Aesthetic Sanitization & De-Templating](#6-aesthetic-sanitization--de-templating)

---

## 1. Inspect & Token Harvesting

### `token-intake` (Figma Conduit)
- **One-Liner:** Extracts live layout geometry, color variables, typographic scales, and spring curves directly from Figma via MCP.
- **When to Use:** When you have a Figma link and need to extract design tokens before writing code.
- **Exact Copy-Paste Prompt:**
  ```text
  Run token-intake on this Figma frame: <FIGMA_URL>. Extract layout properties, spacing tokens, typographic scales, and spring curves into tokens.css.
  ```
- **Inputs & Outputs:** Input: Figma frame URL. Output: `tokens.css` with semantic CSS variables and Tailwind extensions.
- **Foundational Capability:** Live design token inspection & model context protocol extraction.

### `token-harvest`
- **One-Liner:** Scans messy legacy codebases to extract hardcoded hex colors, arbitrary spacing, and font sizes into clean design tokens.
- **When to Use:** When starting work on an existing project with zero centralized token conventions.
- **Exact Copy-Paste Prompt:**
  ```text
  Run token-harvest across src/. Extract all hardcoded colors, spacing classes, and font rules into a unified semantic token file.
  ```
- **Inputs & Outputs:** Input: Source code directory. Output: Consolidated token ledger and refactoring diff.
- **Foundational Capability:** Automated legacy token mining & normalization.

---

## 2. Kinetic Motion Physics (All 20 Skills)

### `motion-choreography`
- **One-Liner:** Constructs animations from scratch following the exact decision hierarchy: gating, runtime tool, composite properties, spring curves, and exits.
- **When to Use:** Adding enter/exit transitions to modals, accordions, dropdowns, and flyout menus.
- **Exact Copy-Paste Prompt:**
  ```text
  Run motion-choreography on <COMPONENT_FILE>. Add enter/exit animations using authentic spring physics. Ensure transitions run on transform/opacity only and include @media (prefers-reduced-motion: reduce).
  ```
- **Inputs & Outputs:** Input: Static component. Output: Animated component with spring physics and composite GPU layers.
- **Foundational Capability:** Full-lifecycle physics-based animation construction.

### `tactile-craft-engineering`
- **One-Liner:** Engineers tactile click depth, active press scales (`0.98`), instant 0ms touch feedback, and micro-physics for buttons and inputs.
- **When to Use:** When buttons, toggles, or cards feel flat, digital, and unresponsive to user touch or clicks.
- **Exact Copy-Paste Prompt:**
  ```text
  Run tactile-craft-engineering on all interactive controls in <COMPONENT_FILE>. Add dampened active press scales, optical focus rings, and instant hover states.
  ```
- **Inputs & Outputs:** Input: Interactive controls. Output: Tactile, physical UI components.
- **Foundational Capability:** Micro-physics affordances and click depth engineering.

### `direct-manipulation`
- **One-Liner:** Implements 1:1 finger tracking, rubber-band resistance past bounds, and velocity-preserving momentum flings.
- **When to Use:** Building draggable sheets, swipe-to-dismiss cards, pull-to-refresh, or drag-to-reorder.
- **Exact Copy-Paste Prompt:**
  ```text
  Run direct-manipulation on <SHEET_OR_DRAWER>. Ensure 1:1 drag tracking, rubber-banding at bounds, and velocity inheritance on release.
  ```
- **Inputs & Outputs:** Input: Gesture surface. Output: Interruptible gesture-driven component.
- **Foundational Capability:** Fluid touch manipulation and gestural spring physics.

### `frame-budget-guard`
- **One-Liner:** Audits animations against the 60fps/120fps frame budget, enforcing composite-only properties (`transform`, `opacity`).
- **When to Use:** When transitions feel janky, stutter on mobile devices, or trigger expensive layout thrashing.
- **Exact Copy-Paste Prompt:**
  ```text
  Run frame-budget-guard on <ANIMATION_FILE>. Eliminate all transitions on height, width, margin, or top/left and move motion off the main thread.
  ```
- **Inputs & Outputs:** Input: CSS or framer-motion code. Output: 60fps-guaranteed composite layer animation code.
- **Foundational Capability:** Compositor layer auditing and GPU frame-budget optimization.

### `toast-mechanics`
- **One-Liner:** Non-blocking notification stacking physics, swipe dismissal, and automatic duration scaling.
- **When to Use:** Adding, styling, or fixing application toast notifications.
- **Exact Copy-Paste Prompt:**
  ```text
  Run toast-mechanics to configure stacked toast notifications in <FILE_PATH> with swipe dismissal, automatic duration scaling, and dark-mode compliance.
  ```
- **Inputs & Outputs:** Input: Notification dispatch logic. Output: Polished notification system.
- **Foundational Capability:** Physics-based notification stacking and gestural dismissal.

### `chaos-ui-tester`
- **One-Liner:** Stress-tests layouts with extreme strings (250+ chars), unbreakable emails, zero counts, and 999999+ values.
- **When to Use:** Auditing tables, cards, and profile screens for text clipping, container blowouts, or broken layouts.
- **Exact Copy-Paste Prompt:**
  ```text
  Run chaos-ui-tester on <COMPONENT_FILE>. Render with edge-case data: 300-character strings, unbreakable URLs, zero counts, and 9999999+ values. Fix all overflow defects.
  ```
- **Inputs & Outputs:** Input: Component under test. Output: Defensively styled component with optical tooltips and robust flex-shrink rules.
- **Foundational Capability:** Chaos UI stress-testing and boundary verification.

### `orchestrate-sequences`
- **One-Liner:** Coordinates multi-element staggered entrances and shared-element transitions so groups read as one intentional motion.
- **When to Use:** Staggered list reveals, dashboard card loading sequences, and multi-step view transitions.
- **Exact Copy-Paste Prompt:**
  ```text
  Run orchestrate-sequences on <LIST_OR_GRID>. Coordinate staggered entrances with 40ms stagger delays, natural overlap, and shared layout keys.
  ```
- **Inputs & Outputs:** Input: Multi-element collection. Output: Coordinated entrance sequence.
- **Foundational Capability:** Multi-element motion choreography and stagger timing.

### `mobile-physics-expo`
- **One-Liner:** Native React Native and Expo spring physics, gesture handling, and haptic feedback.
- **When to Use:** Building animations in Expo/React Native apps with Reanimated and Gesture Handler.
- **Exact Copy-Paste Prompt:**
  ```text
  Run mobile-physics-expo on <REACT_NATIVE_SCREEN>. Wire up Reanimated spring transitions on the UI thread with expo-haptics feedback.
  ```
- **Inputs & Outputs:** Input: React Native view. Output: Native-thread gesture and animation code.
- **Foundational Capability:** Mobile-native spring physics and haptic integration.

### `cupertino-physicality`
- **One-Liner:** Translates Apple Human Interface Guidelines fluid motion and translucent materials to the web.
- **When to Use:** Building iOS-style sheets, momentum carousels, or Apple-tier tactile interfaces.
- **Exact Copy-Paste Prompt:**
  ```text
  Run cupertino-physicality on <COMPONENT>. Implement fluid Apple-style spring curves, momentum deceleration, and optical typography tracking.
  ```
- **Inputs & Outputs:** Input: Web component. Output: Apple-grade tactile interaction code.
- **Foundational Capability:** Apple HIG gestural physical standards.

### `motion-advisor`
- **One-Liner:** Consultative design engineering diagnostics for stiff, robotic, or artificial interface motion.
- **When to Use:** When you know an animation feels wrong but can't pinpoint why.
- **Exact Copy-Paste Prompt:**
  ```text
  Run motion-advisor to evaluate why <COMPONENT> feels sluggish and unnatural. Recommend exact curve parameters and durations.
  ```
- **Inputs & Outputs:** Input: Existing animation code. Output: Expert diagnosis and tuned parameter table.
- **Foundational Capability:** Expert motion critique and advisory.

### `discover-motion-gaps`
- **One-Liner:** Scans codebases to identify static, dead interactions that demand physical feedback.
- **When to Use:** During a design engineering pass to find where micro-interactions will elevate the product.
- **Exact Copy-Paste Prompt:**
  ```text
  Run discover-motion-gaps across src/components/. Identify all static interactive elements that need tactile feedback.
  ```
- **Inputs & Outputs:** Input: Component directory. Output: Prioritized motion opportunity roadmap.
- **Foundational Capability:** Proactive interaction opportunity discovery.

### `motion-overhaul`
- **One-Liner:** Full codebase motion audit producing a prioritized roadmap of animation fixes.
- **When to Use:** When an entire application feels laggy, choppy, or over-animated.
- **Exact Copy-Paste Prompt:**
  ```text
  Run motion-overhaul on current codebase. Audit all CSS transitions and Framer Motion instances. Generate prioritized remediation roadmap.
  ```
- **Inputs & Outputs:** Input: Project repository. Output: Comprehensive motion audit report and fix schedule.
- **Foundational Capability:** Codebase-wide animation audit and refactoring architecture.

### `motion-restraint`
- **One-Liner:** Subtractive engineering: finding and purging sluggish, annoying, or unnecessary animations.
- **When to Use:** When users complain an app feels slow or has "too much animation going on".
- **Exact Copy-Paste Prompt:**
  ```text
  Run motion-restraint to prune unnecessary animations in <FILE_OR_DIR>. Remove motion on keyboard shortcuts, high-frequency tables, and decorative clutter.
  ```
- **Inputs & Outputs:** Input: Over-animated component. Output: Lean, instant, performant UI code.
- **Foundational Capability:** Subtractive motion pruning and velocity optimization.

### `motion-critique`
- **One-Liner:** Senior design engineering code review for animation pull requests and diffs.
- **When to Use:** Reviewing a teammate's PR or evaluating your own motion changes before merging.
- **Exact Copy-Paste Prompt:**
  ```text
  Run motion-critique on git diff. Audit curves, durations, composite layer safety, and reduced-motion handling.
  ```
- **Inputs & Outputs:** Input: Git diff or pull request. Output: Line-by-line review comments and code patches.
- **Foundational Capability:** Senior motion code review and quality gate enforcement.

### `motion-lexicon`
- **One-Liner:** Reverse glossary translating vague physical descriptions into exact engineering terms.
- **When to Use:** When you know how you want an effect to feel but don't know the CSS/Framer term.
- **Exact Copy-Paste Prompt:**
  ```text
  Run motion-lexicon: What is the term for 'when a drawer bounces back when pulled too far'?
  ```
- **Inputs & Outputs:** Input: Plain English description. Output: Technical term, timing curve, and implementation snippet.
- **Foundational Capability:** Reverse-lookup motion engineering terminology.

### `touch-fidelity`
- **One-Liner:** Eliminates webview quirks (sticky hover states, 100vh bugs, tap highlight flashes) to achieve authentic app feel.
- **When to Use:** When a web app feels like an amateur website in mobile Chrome or Safari.
- **Exact Copy-Paste Prompt:**
  ```text
  Run touch-fidelity on src/styles/globals.css and mobile layouts. Fix tap highlight flashes, notch insets, and touch delay.
  ```
- **Inputs & Outputs:** Input: Mobile web styles. Output: Native-feeling touch web app code.
- **Foundational Capability:** Mobile webview native-fidelity engineering.

### `cultivate-aesthetic`
- **One-Liner:** Educational mental models for developing design discernment and avoiding cheap flashiness.
- **When to Use:** When designing a flagship product and seeking high-taste visual principles.
- **Exact Copy-Paste Prompt:**
  ```text
  Run cultivate-aesthetic on this proposed concept: <CONCEPT>. Evaluate whether it passes the test of timeless software craft.
  ```
- **Inputs & Outputs:** Input: Design proposal. Output: Deep design critique and elevation strategy.
- **Foundational Capability:** Design engineering taste cultivation and discernment.

### `primitive-evaluator`
- **One-Liner:** Objective architectural evaluation of headless UI primitives (Radix, React Aria, Base UI, Ark).
- **When to Use:** Starting a new frontend project and deciding which component library to build on.
- **Exact Copy-Paste Prompt:**
  ```text
  Run primitive-evaluator for our stack: <FRAMEWORK_AND_REQUIREMENTS>. Recommend the best headless primitive library with trade-off analysis.
  ```
- **Inputs & Outputs:** Input: Project technical requirements. Output: Library recommendation and architectural trade-off matrix.
- **Foundational Capability:** Component library evaluation and architecture selection.

### `rapid-harness`
- **One-Liner:** Rapid throwaway interaction sandbox for testing physical feel before writing production code.
- **When to Use:** Experimenting with complex gesture flings or custom shaders.
- **Exact Copy-Paste Prompt:**
  ```text
  Run rapid-harness to build a throwaway sandbox for testing <EXPERIMENTAL_INTERACTION>.
  ```
- **Inputs & Outputs:** Input: Experimental interaction concept. Output: Self-contained prototype testbed.
- **Foundational Capability:** Rapid experimental prototyping harness.

### `swiftui-motion-patterns`
- **One-Liner:** Idiomatic Swift 6 and SwiftUI gesture and animation architectures.
- **When to Use:** Writing modern iOS apps with SwiftUI animation and gesture handlers.
- **Exact Copy-Paste Prompt:**
  ```text
  Run swiftui-motion-patterns on <SWIFT_VIEW>. Implement interactive spring animations with Swift 6 data-race safety.
  ```
- **Inputs & Outputs:** Input: SwiftUI View. Output: Modern SwiftUI animation code.
- **Foundational Capability:** Modern Swift 6 / SwiftUI fluid animation design.

---

## 3. Structural Rigor & UX Architecture

### `blueprint`
- **One-Liner:** Determines surface mode (Workspace, Editorial, Reading) and maps spatial container topology.
- **When to Use:** Starting any new page or major screen redesign.
- **Exact Copy-Paste Prompt:**
  ```text
  Run blueprint on <FEATURE_SPEC>. Determine the surface mode, map container zones, and structure information hierarchy.
  ```
- **Inputs & Outputs:** Input: Feature brief. Output: Wireframe architecture and surface mode specification.
- **Foundational Capability:** UX architecture & mode selection engine.

### `spatial-cadence`
- **One-Liner:** Establishes geometric grid rhythm, equal margin alignment, and fluid responsive breakpoints.
- **When to Use:** Fixing misaligned layouts or broken responsive scaling.
- **Exact Copy-Paste Prompt:**
  ```text
  Run spatial-cadence on <LAYOUT_FILE>. Enforce equal left/right margins and fluid responsive breakpoints at 390px, 768px, 1024px, and 1440px.
  ```
- **Inputs & Outputs:** Input: Layout code. Output: Balanced responsive CSS grid/flexbox code.
- **Foundational Capability:** Geometric grid layout & breakpoint balance.

### `type-discipline`
- **One-Liner:** Enforces optical sizing, modular type scales, and line-height geometry.
- **When to Use:** Auditing typography for illegibility, uneven line spacing, or inconsistent heading tiers.
- **Exact Copy-Paste Prompt:**
  ```text
  Run type-discipline on src/styles/typography.css. Enforce modular typographic scale, optical sizes, and 65ch line lengths for body text.
  ```
- **Inputs & Outputs:** Input: Typographic rules. Output: Cohesive modular type system.
- **Foundational Capability:** Typographic hierarchy and optical scale enforcement.

### `chroma-curate`
- **One-Liner:** Structures disciplined color ramps, contrast ratios, and semantic token assignments.
- **When to Use:** Fixing chaotic color palettes or poor WCAG contrast ratios.
- **Exact Copy-Paste Prompt:**
  ```text
  Run chroma-curate on the color palette. Ensure tinted neutrals, 1 primary accent, and 4.5:1 minimum contrast for text.
  ```
- **Inputs & Outputs:** Input: Color tokens. Output: Harmonious semantic color ramp.
- **Foundational Capability:** Systematic color ramp curation and token assignment.

### `amplify-weight` & `subdue-presence`
- **One-Liner:** Selectively dials visual weight and contrast up (bolder) or down (quieter).
- **When to Use:** When a page feels bland and timid (`amplify-weight`), or visually chaotic and loud (`subdue-presence`).
- **Exact Copy-Paste Prompt:**
  ```text
  Run amplify-weight on <SECTION> to increase typographic hierarchy and visual punch.
  # OR
  Run subdue-presence on <SECTION> to calm visual noise and soften high contrast.
  ```
- **Inputs & Outputs:** Input: Component styles. Output: Calibrated visual presence.
- **Foundational Capability:** Visual weight and cognitive density calibration.

---

## 4. Editorial Cadence & Layout Rhythm

### `editorial-craft`
- **One-Liner:** Anti-slop visual layout engine enforcing 1-section-per-screen rhythm (1440x900) and punchy copywriting.
- **When to Use:** Building or auditing landing pages, company websites, and product flagships.
- **Exact Copy-Paste Prompt:**
  ```text
  Run editorial-craft on <PAGE_FILE>. Enforce the 1-section-per-screen rule, eliminate all corporate buzzwords, and write declarative copy.
  ```
- **Inputs & Outputs:** Input: Landing page code. Output: Screen-filling visual sections with authentic brand copywriting.
- **Foundational Capability:** Anti-slop landing page architecture and layout rhythm.

### `prose-architecture`
- **One-Liner:** Writes declarative, authentic brand copy with zero marketing fluff ('supercharge', 'seamless').
- **When to Use:** Rewriting marketing text to sound human, confident, and direct.
- **Exact Copy-Paste Prompt:**
  ```text
  Run prose-architecture on <LANDING_PAGE>. Strip all corporate jargon and rewrite headers to state plainly what is built and why it matters.
  ```
- **Inputs & Outputs:** Input: Marketing draft. Output: Punchy, authoritative brand copy.
- **Foundational Capability:** High-conviction editorial copywriting.

### `signature-interactions`
- **One-Liner:** Designs 1–2 unforgettable interactive moments on a page.
- **When to Use:** Adding a memorable interactive showcase to a landing page hero or feature section.
- **Exact Copy-Paste Prompt:**
  ```text
  Run signature-interactions for <PRODUCT_HERO>. Design and build a bespoke tactile interactive centerpiece that proves product value.
  ```
- **Inputs & Outputs:** Input: Feature concept. Output: Interactive React/Tailwind component with physics-based feedback.
- **Foundational Capability:** Memorable interactive moment design.

---

## 5. Defensive Fortification

### `fortify`
- **One-Liner:** Battle-tests interfaces against missing data, boundary conditions, network latency, and accessibility barriers.
- **When to Use:** Pre-production hardening of components, forms, tables, and views.
- **Exact Copy-Paste Prompt:**
  ```text
  Run fortify on <COMPONENT_OR_PAGE>. Implement zero-state empty views, zero-CLS skeleton loaders, error recovery bounds, and WCAG AA focus indicators.
  ```
- **Inputs & Outputs:** Input: Production candidate component. Output: Hardened component with full fault-state coverage.
- **Foundational Capability:** Defensive edge-case engineering and accessibility hardening.

### `finish-standards`
- **One-Liner:** Pre-flight release quality gate enforcing browser-tested rendering at 1440, 1024, 768, and 390.
- **When to Use:** Final check before deploying UI code to production.
- **Exact Copy-Paste Prompt:**
  ```text
  Run finish-standards audit on <PRODUCTION_PAGE>. Verify zero empty grounds, zero text clipping, and responsive parity across all breakpoints.
  ```
- **Inputs & Outputs:** Input: Built page. Output: Pre-flight checklist report and pass/fail certification.
- **Foundational Capability:** Pre-release quality gate and visual verification.

---

## 6. Aesthetic Sanitization & De-Templating

### `de-generic`
- **One-Liner:** Purges generic AI generator tells: purple gradient halos, glossy emoji badges, blurry glassmorphism, and flat type.
- **When to Use:** When a v0, Lovable, Bolt, or AI-generated interface looks synthetic, amateurish, or template-like.
- **Exact Copy-Paste Prompt:**
  ```text
  Run de-generic on <PAGE_OR_PROJECT>. Strip out all purple mesh gradients, floating emoji chips, and generic three-card feature rows. Replace with bespoke typography and authentic brand styling.
  ```
- **Inputs & Outputs:** Input: AI-generated code. Output: Cleaned, bespoke interface with senior human craft aesthetic.
- **Foundational Capability:** Aesthetic de-templating and anti-artifact sanitization.

### `filter-artifacts`
- **One-Liner:** Eliminates gratuitous CSS glow effects, neon blobs, and unreadable glassmorphic backdrop filters.
- **When to Use:** Cleaning up visual pollution and low-contrast text on card surfaces.
- **Exact Copy-Paste Prompt:**
  ```text
  Run filter-artifacts across <STYLES_OR_COMPONENTS>. Replace blurred gradient blobs with crisp neutral borders and authentic physical shadows.
  ```
- **Inputs & Outputs:** Input: Over-styled CSS/Tailwind classes. Output: High-contrast, clean visual styling.
- **Foundational Capability:** Visual noise reduction and optical cleanup.

### `hallmark-smells`
- **One-Liner:** Audits code against an exhaustive catalogue of instant visual red flags that give away uncurated AI code.
- **When to Use:** Running a redline review on newly generated code.
- **Exact Copy-Paste Prompt:**
  ```text
  Run hallmark-smells on <NEW_COMPONENT>. Identify any AI generation tells (pulsing static buttons, emoji badges, low-contrast text).
  ```
- **Inputs & Outputs:** Input: Component source. Output: Redline defect list with exact file and line numbers.
- **Foundational Capability:** AI template tell detection.
