# OpusForge Disciplines Catalog (`DISCIPLINES-CATALOG.md`)

When you don't need the entire 6-stage flagship pipeline (`opus-pipeline`), you can invoke any single discipline independently to solve a focused engineering problem — such as tuning a modal spring, stress-testing extreme strings, writing bespoke copy, or eliminating generic AI gradient halos.

---

## 1. Inspect & Token Intake

### `token-intake` (Figma Conduit)
- **One-Liner:** Extracts live design tokens, container dimensions, and prototype spring curves directly from Figma via MCP.
- **When to Use:** When you have a Figma file or frame link and need production-grade CSS tokens before coding.
- **Copy-Paste Prompt:**
  ```text
  Run token-intake on this Figma frame: <FIGMA_URL>. Extract layout properties, spacing tokens, typographic scales, and spring curves into tokens.css.
  ```
- **Inputs & Outputs:** Input: Figma frame URL. Output: `tokens.css` with semantic CSS variables and Tailwind extensions.
- **Original Capability:** Figma MCP live token extraction and frame inspection.

### `token-harvest`
- **One-Liner:** Scans existing source files to harvest recurring hex colors, arbitrary spacing values, and fonts into structured design tokens.
- **When to Use:** When refactoring a messy existing project that lacks a centralized token system.
- **Copy-Paste Prompt:**
  ```text
  Run token-harvest across src/. Extract all hardcoded colors, spacing classes, and font rules into a unified semantic token file.
  ```
- **Inputs & Outputs:** Input: Source code directory. Output: Consolidated token ledger and refactoring diff.
- **Original Capability:** structural-rigor extraction engine.

---

## 2. Architect & UX Topology

### `blueprint`
- **One-Liner:** Architects information topology, container constraints, and selects the optimal surface mode (Workspace, Editorial, or Reading).
- **When to Use:** At the start of designing a new page, feature flow, or major screen redesign.
- **Copy-Paste Prompt:**
  ```text
  Run blueprint on this user story: <FEATURE_DESCRIPTION>. Determine the surface mode (Workspace, Editorial, or Reading), map the spatial container zones, and structure the information hierarchy.
  ```
- **Inputs & Outputs:** Input: Feature brief or user story. Output: Structured layout wireframe and surface mode specification.
- **Original Capability:** structural-rigor shape workflow.

### `spatial-cadence`
- **One-Liner:** Establishes geometric grid rhythm, equal margin alignment, and fluid responsive breakpoints.
- **When to Use:** When layout elements feel misaligned, cramped, or collapse awkwardly on mobile viewports.
- **Copy-Paste Prompt:**
  ```text
  Run spatial-cadence on <COMPONENT_FILE>. Enforce equal left/right margins, consistent flex/grid gaps, and responsive breakpoints at 390px, 768px, 1024px, and 1440px.
  ```
- **Inputs & Outputs:** Input: Component or page layout file. Output: Corrected CSS grid/flexbox code.
- **Original Capability:** structural-rigor layout engine.

---

## 3. Layout & Editorial Copywriting

### `editorial-craft`
- **One-Liner:** Anti-slop visual layout engine enforcing one-section-per-screen rhythm and distinctive brand copywriting.
- **When to Use:** Building or reviewing landing pages, product homepages, or company flagships.
- **Copy-Paste Prompt:**
  ```text
  Run editorial-craft on this landing page: <PAGE_FILE>. Ensure the hero occupies viewport 1 alone at 1440x900, eliminate all corporate buzzwords, and write declarative, punchy copy.
  ```
- **Inputs & Outputs:** Input: Page source or content outline. Output: Screen-filling section markup with authentic human copywriting.
- **Original Capability:** editorial-craft anti-slop engine.

### `signature-interactions`
- **One-Liner:** Designs 1–2 unforgettable interactive moments on a page (dropzones, interactive telemetry, physics visualizers).
- **When to Use:** When a landing page or product UI is clean but lacks a memorable interactive centerpiece.
- **Copy-Paste Prompt:**
  ```text
  Run signature-interactions for this feature: <PRODUCT_CONCEPT>. Design and implement a bespoke tactile interactive moment that demonstrates the product's core value.
  ```
- **Inputs & Outputs:** Input: Feature concept. Output: Interactive React/Tailwind component with physics-based feedback.
- **Original Capability:** editorial-craft moments architecture.

---

## 4. Kinetic Motion Physics

### `motion-choreography`
- **One-Liner:** Builds end-to-end physics-based animations with proper triggers, spring parameters, and interruptible exits.
- **When to Use:** When animating an element from scratch (dropdown, accordion, sheet, hero entrance).
- **Copy-Paste Prompt:**
  ```text
  Run motion-choreography on this component: <COMPONENT_FILE>. Add enter/exit animations using authentic spring physics. Ensure transitions run on composite properties and respect prefers-reduced-motion.
  ```
- **Inputs & Outputs:** Input: Static component. Output: Animated component with spring physics and composite GPU layers.
- **Original Capability:** Emil Kowalski animate skill.

### `tactile-craft-engineering`
- **One-Liner:** Adds authentic tactile feedback, click depth (active press scale 0.98), and micro-physics to interactive controls.
- **When to Use:** When buttons, toggles, or cards feel flat, digital, and unresponsive to user touch or clicks.
- **Copy-Paste Prompt:**
  ```text
  Run tactile-craft-engineering on all interactive controls in <COMPONENT_FILE>. Add dampened active press scales, optical focus rings, and instant hover states.
  ```
- **Inputs & Outputs:** Input: Button/form controls. Output: High-tactility interactive elements.
- **Original Capability:** Emil Kowalski design engineering philosophy.

### `direct-manipulation`
- **One-Liner:** Builds 1:1 finger/mouse tracking gestures, bottom sheets, swipe-to-dismiss, and momentum flings.
- **When to Use:** Building mobile-friendly drawers, modal sheets, or draggable list items.
- **Copy-Paste Prompt:**
  ```text
  Run direct-manipulation to build a bottom sheet drawer in <FILE_PATH>. Ensure 1:1 drag tracking, rubber-banding at bounds, and velocity inheritance on release.
  ```
- **Inputs & Outputs:** Input: Sheet container. Output: Interruptible gesture-driven component.
- **Original Capability:** Emil Kowalski gestures skill.

### `toast-mechanics`
- **One-Liner:** Implements non-blocking stacked notifications with swipe dismissal and physics-based expansion.
- **When to Use:** Integrating or troubleshooting notification toasts in web applications.
- **Copy-Paste Prompt:**
  ```text
  Run toast-mechanics in <FILE_PATH>. Configure stacked toast notifications with swipe dismissal, automatic duration scaling, and dark-mode compliance.
  ```
- **Inputs & Outputs:** Input: Toast container / dispatch logic. Output: Polished notification system.
- **Original Capability:** Emil Kowalski ask-sonner skill.

---

## 5. Defensive Fortification

### `fortify`
- **One-Liner:** Battle-tests interfaces against missing data, boundary conditions, network latency, and accessibility failures.
- **When to Use:** Before deploying any component to production or staging.
- **Copy-Paste Prompt:**
  ```text
  Run fortify on <COMPONENT_OR_PAGE>. Implement zero-state empty views, zero-CLS skeleton loaders, error recovery bounds, and WCAG AA keyboard focus indicators.
  ```
- **Inputs & Outputs:** Input: Production candidate component. Output: Hardened component with full fault-state coverage.
- **Original Capability:** structural-rigor harden workflow.

### `chaos-ui-tester`
- **One-Liner:** Stress-tests layouts against worst-case strings (250+ chars), unbreakable emails, extreme numbers, and non-Latin scripts.
- **When to Use:** Auditing components for text clipping, container blowouts, or broken table layouts.
- **Copy-Paste Prompt:**
  ```text
  Run chaos-ui-tester on <COMPONENT_FILE>. Render with edge-case data: 300-character strings, unbreakable URLs, zero counts, and 9999999+ values. Fix all overflow defects.
  ```
- **Inputs & Outputs:** Input: Component under test. Output: Defensively styled component with optical tooltips and robust flex-shrink rules.
- **Original Capability:** Emil Kowalski break-ui skill.

---

## 6. Aesthetic Sanitization & De-Templating

### `de-generic`
- **One-Liner:** Purges generic AI generator tells: purple gradient halos, glossy emoji badges, blurry glassmorphism, and flat type.
- **When to Use:** When a v0, Lovable, Bolt, or AI-generated interface looks synthetic, amateurish, or template-like.
- **Copy-Paste Prompt:**
  ```text
  Run de-generic on <PAGE_OR_PROJECT>. Strip out all purple mesh gradients, floating emoji chips, and generic three-card feature rows. Replace with bespoke typography and authentic brand styling.
  ```
- **Inputs & Outputs:** Input: AI-generated code. Output: Cleaned, bespoke interface with senior human craft aesthetic.
- **Original Capability:** de-generic de-slop engine.

### `filter-artifacts`
- **One-Liner:** Eliminates gratuitous CSS glow effects, neon blobs, and unreadable glassmorphic backdrop filters.
- **When to Use:** Cleaning up visual pollution and low-contrast text on card surfaces.
- **Copy-Paste Prompt:**
  ```text
  Run filter-artifacts across <STYLES_OR_COMPONENTS>. Replace blurred gradient blobs with crisp neutral borders and authentic physical shadows.
  ```
- **Inputs & Outputs:** Input: Over-styled CSS/Tailwind classes. Output: High-contrast, clean visual styling.
- **Original Capability:** de-generic effects reference.
