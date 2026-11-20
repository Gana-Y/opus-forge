# OpusForge (`opus-forge`)

> **The Sovereign Full-Stack AI Design Engineering & Interface Hardening Engine**  
> *Transform raw requirements into human-grade, million-dollar web flagships.*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![MCP: Figma](https://img.shields.io/badge/MCP-Figma_Bridge-purple.svg)](disciplines/figma-conduit/SETUP.md)
[![Disciplines: 35+](https://img.shields.io/badge/Disciplines-35+_Documented-emerald.svg)](DISCIPLINES-CATALOG.md)
[![Framerate: 60/120fps](https://img.shields.io/badge/Framerate-60%2F120fps_Guaranteed-orange.svg)](disciplines/kinetic-physics/frame-budget-guard/SKILL.md)

---

## Table of Contents
1. [The Problem with Current AI Design Repositories](#the-problem-with-current-ai-design-repositories)
2. [How to Install OpusForge in Your Workspace](#how-to-install-opusforge-in-your-workspace)
   - [Method A: Add to an Existing Coding Project](#method-a-add-to-an-existing-coding-project-react-nextjs-vite)
   - [Method B: Install Globally into AI Agents](#method-b-install-globally-into-ai-agents-antigravity-claude-cursor)
3. [The "What to Type" Prompt Cookbook](#the-what-to-type-prompt-cookbook)
   - [Scenario 1: Build a Whole Website from a Figma Link](#scenario-1-build-a-whole-website-from-a-figma-link)
   - [Scenario 2: Clean Up an Ugly / Generic AI Project](#scenario-2-clean-up-an-ugly--generic-ai-project-de-slop)
   - [Scenario 3: Animate a Single Component (Button, Modal, Sheet)](#scenario-3-animate-a-single-component-button-modal-sheet)
   - [Scenario 4: Harden an Existing Component Against Edge Cases](#scenario-4-harden-an-existing-component-against-edge-cases)
   - [Scenario 5: Write Punchy Copy & Fix Section Spacing](#scenario-5-write-punchy-copy--fix-section-spacing)
4. [Exhaustive Skills & Disciplines Directory](#exhaustive-skills--disciplines-directory)
   - [Master Autonomous Pipeline](#1-master-autonomous-pipeline)
   - [Figma Token Intake](#2-figma-token-intake)
   - [Kinetic Motion Physics (All 20 Skills)](#3-kinetic-motion-physics-all-20-skills)
   - [Structural Rigor & UX Architecture](#4-structural-rigor--ux-architecture)
   - [Editorial Cadence & Layout Rhythm](#5-editorial-cadence--layout-rhythm)
   - [Aesthetic Sanitization & De-Templating](#6-aesthetic-sanitization--de-templating)
5. [Step-by-Step Walkthroughs](#step-by-step-walkthroughs)
   - [How to Use for a Single Component](#how-to-use-opusforge-for-a-single-component)
   - [How to Use for a Complete Website](#how-to-use-opusforge-for-a-complete-website)
6. [Repository Architecture](#repository-architecture)
7. [Credits & Attribution](#credits--upstream-attribution)

---

## The Problem with Current AI Design Repositories

When you clone the individual repositories floating around GitHub, you hit a brick wall:
- **No integration guide:** They dump loose markdown files without explaining where to put them or how an AI reads them.
- **No command cookbook:** You are left guessing what phrase to type into your chat prompt to actually trigger the behavior.
- **Fragmented workflows:** You have to manually hop between one repo for animations, another for copywriting, another for layouts, and another for edge cases.

**OpusForge solves this completely.** It unifies all disciplines into ONE cohesive architecture, provides an autonomous 6-stage master pipeline for full builds, and gives you an explicit copy-paste prompt cookbook for every standalone component task.

---

## How to Install OpusForge in Your Workspace

### Method A: Add to an Existing Coding Project (React, Next.js, Vite)
If you already have a repository (e.g., `my-saas-app`, `portfolio`, `e-commerce`):

1. **Clone OpusForge into a `.skills/` or `skills/` folder inside your project:**
   ```bash
   cd my-saas-app
   git clone https://github.com/Gana-Y/opus-forge.git .skills/opus-forge
   ```

2. **Tell your AI assistant (Antigravity / Cursor / Claude Code):**
   > *"I have installed OpusForge under `.skills/opus-forge/disciplines/`. Read the disciplines there whenever I ask you to build, animate, harden, or polish UI components."*

Your assistant now has immediate access to all 35+ disciplines, references, token schemas, and checklists.

---

### Method B: Install Globally into AI Agents (Antigravity, Claude, Cursor)

#### For Google Antigravity:
Copy or link OpusForge into your Antigravity skills directory:
```powershell
# Windows
Copy-Item -Recurse "opus-forge\disciplines\*" "$HOME\.gemini\config\skills"

# macOS / Linux
cp -r opus-forge/disciplines/* ~/.gemini/config/skills/
```

#### For Claude Code / Claude Desktop:
```bash
cp -r opus-forge/disciplines/* ~/.claude/skills/
```

#### For Cursor / Windsurf:
Add the path to your `.cursorrules` or workspace settings:
```json
{
  "cursor.agentSkills": [
    "./.skills/opus-forge/disciplines"
  ]
}
```

---

## The "What to Type" Prompt Cookbook

Here is the exact copy-paste cheatsheet for everyday development:

### Scenario 1: Build a Whole Website from a Figma Link
> **What to type in chat:**
> ```text
> opus-pipeline full-build for https://www.figma.com/design/:fileKey/:fileName?node-id=1:675
> Follow all 6 stages sequentially: Token Intake -> UX Blueprint -> Editorial Craft -> Kinetic Polish -> Fortify -> De-Generic. Show verification evidence at each gate.
> ```

---

### Scenario 2: Clean Up an Ugly / Generic AI Project (De-Slop)
When a page built with v0, Lovable, or Bolt has purple glows, floating emoji chips, and generic templates:
> **What to type in chat:**
> ```text
> Run de-generic on src/app/page.tsx.
> Strip out all purple/violet gradient overlays, floating emoji badges ("New ✨"), and centered three-box cards. Replace with high-contrast neutral borders, bespoke typography, and authentic product previews per OpusForge aesthetic sanitizer rules.
> ```

---

### Scenario 3: Animate a Single Component (Button, Modal, Sheet)
> **For a Button (Click depth & tactile feel):**
> ```text
> Run tactile-craft-engineering on src/components/Button.tsx.
> Add active click depth with scale(0.98), instant press response, dampened spring release, and high-visibility :focus-visible rings.
> ```

> **For a Modal / Dialog:**
> ```text
> Run motion-choreography on src/components/Modal.tsx.
> Implement backdrop opacity fade and dialog entrance translation using spring physics. Ensure transitions run on transform/opacity only and include @media (prefers-reduced-motion: reduce).
> ```

> **For a Draggable Bottom Sheet:**
> ```text
> Run direct-manipulation on src/components/BottomSheet.tsx.
> Implement 1:1 finger tracking, rubber-band resistance past bounds, and velocity-preserving flings on release.
> ```

---

### Scenario 4: Harden an Existing Component Against Edge Cases
> **What to type in chat:**
> ```text
> Run fortify and chaos-ui-tester on src/components/UserTable.tsx.
> Test with worst-case data: 250-character strings, unbreakable URLs, zero items, and 999999+ counts. Implement skeleton loading states (CLS = 0), inline error recovery boundaries, and full keyboard tab traversal.
> ```

---

### Scenario 5: Write Punchy Copy & Fix Section Spacing
> **What to type in chat:**
> ```text
> Run editorial-craft on src/components/Hero.tsx and src/components/Features.tsx.
> Enforce the strict 'one section per screen' rule at 1440x900. Rewrite all headlines and body text to eliminate corporate buzzwords ('supercharge', 'seamless', 'all-in-one'). Write plain, declarative copy with an unmistakable point of view.
> ```

---

## Exhaustive Skills & Disciplines Directory

Every discipline in OpusForge is categorized below with its exact purpose and invocation prompt:

### 1. Master Autonomous Pipeline
| Discipline | Description | Exact Copy-Paste Prompt |
|:---|:---|:---|
| **`opus-pipeline`** | Autonomous 6-stage master website build orchestrator. | `opus-pipeline full-build for <FIGMA_OR_BRIEF>` |

---

### 2. Figma Token Intake
| Discipline | Description | Exact Copy-Paste Prompt |
|:---|:---|:---|
| **`token-intake`** | Extracts live tokens, frames, and motion curves via Figma MCP. | `Run token-intake on <FIGMA_FRAME_URL>` |
| **`token-harvest`** | Mins hardcoded hex colors and spacing classes from existing code. | `Run token-harvest across src/ and compile tokens.css` |

---

### 3. Kinetic Motion Physics (All 20 Skills)
| Discipline | Description | Exact Copy-Paste Prompt |
|:---|:---|:---|
| **`motion-choreography`** | Full-lifecycle animation engineering (triggers, curves, exits). | `Run motion-choreography on <COMPONENT_FILE>` |
| **`tactile-craft-engineering`** | Micro-physics, click depths (scale 0.98), and tactile affordances. | `Run tactile-craft-engineering on <CONTROLS>` |
| **`direct-manipulation`** | 1:1 gesture tracking, bottom sheets, and momentum flings. | `Run direct-manipulation on <SHEET_OR_DRAWER>` |
| **`frame-budget-guard`** | 60fps/120fps composite layer audits and jank diagnostics. | `Run frame-budget-guard on <ANIMATION_FILE>` |
| **`toast-mechanics`** | Non-blocking stacked notifications with swipe dismissal. | `Run toast-mechanics to configure notification system` |
| **`chaos-ui-tester`** | Stress-testing layouts with extreme strings and broken data. | `Run chaos-ui-tester on <COMPONENT_FILE>` |
| **`orchestrate-sequences`** | Coordinating multi-element staggered entrances and shared transitions. | `Run orchestrate-sequences on <LIST_OR_GRID>` |
| **`mobile-physics-expo`** | Native React Native & Expo gestural springs and haptics. | `Run mobile-physics-expo on <REACT_NATIVE_SCREEN>` |
| **`cupertino-physicality`** | Fluid, continuous, interruptible Apple HIG motion standards. | `Run cupertino-physicality on <GESTURAL_UI>` |
| **`motion-advisor`** | Consultative diagnostics for stiff or robotic interface feel. | `Run motion-advisor to diagnose why <COMPONENT> feels laggy` |
| **`discover-motion-gaps`** | Locates static UI surfaces that demand physical feedback. | `Run discover-motion-gaps across <PROJECT_DIR>` |
| **`motion-overhaul`** | Comprehensive audit and refactoring roadmap for interface motion. | `Run motion-overhaul on current codebase` |
| **`motion-restraint`** | Subtractive engineering: purging sluggish or annoying animations. | `Run motion-restraint to prune unnecessary motion in <FILE>` |
| **`motion-critique`** | Senior motion engineering code review for PRs and diffs. | `Run motion-critique on git diff` |
| **`motion-lexicon`** | Reverse glossary translating vague motion ideas to exact terms. | `Run motion-lexicon for <DESCRIBED_EFFECT>` |
| **`touch-fidelity`** | Eliminates webview quirks to produce authentic installed-app feel. | `Run touch-fidelity on mobile web layout` |
| **`cultivate-aesthetic`** | Distinguishing high-craft motion from cheap, distracting flashiness. | `Run cultivate-aesthetic to evaluate motion choices` |
| **`primitive-evaluator`** | Objective evaluation of headless UI primitives and motion libraries. | `Run primitive-evaluator for <PROJECT_REQUIREMENTS>` |
| **`rapid-harness`** | Rapid throwaway interaction sandbox for testing physical feel. | `Run rapid-harness to prototype <INTERACTION>` |
| **`swiftui-motion-patterns`** | Modern Swift 6 and SwiftUI gesture and animation architectures. | `Run swiftui-motion-patterns on <SWIFT_VIEW>` |

---

### 4. Structural Rigor & UX Architecture
| Discipline | Description | Exact Copy-Paste Prompt |
|:---|:---|:---|
| **`blueprint`** | Information topology and surface mode selection (Workspace/Editorial/Reading). | `Run blueprint on <FEATURE_SPEC>` |
| **`fortify`** | Edge-case defense, error boundaries, empty states, and accessibility. | `Run fortify on <COMPONENT_OR_PAGE>` |
| **`audit-rubric`** | Senior design evaluation criteria against world-class benchmarks. | `Run audit-rubric on <SCREEN_OR_ROUTE>` |
| **`micro-refine`** | Sub-pixel alignment, border-radius nesting, and token harmonization sweeps. | `Run micro-refine across <COMPONENT_STYLES>` |
| **`spatial-cadence`** | Grid alignments, margin balance, and fluid breakpoint logic. | `Run spatial-cadence on <LAYOUT_CONTAINER>` |
| **`type-discipline`** | Optical sizing, modular type scales, and line-height geometry. | `Run type-discipline on typographic styles` |
| **`chroma-curate`** | Coherent color ramps, contrast ratios, and semantic token roles. | `Run chroma-curate on color palette` |
| **`sensory-spark`** | Memorable, earned micro-interactions and tactile reward moments. | `Run sensory-spark on <INTERACTIVE_MOMENT>` |
| **`amplify-weight`** | Enhances typographic weight, contrast, and visual presence. | `Run amplify-weight to make <SECTION> bolder` |
| **`subdue-presence`** | Calms visual chaos, lowers density, and softens excessive contrast. | `Run subdue-presence to make <PAGE> quieter` |
| **`prune-density`** | Strips extraneous decorative chrome to amplify core utility. | `Run prune-density on <DENSE_DASHBOARD>` |
| **`demist-ui`** | Eliminates ambiguous labeling and weak interactive signifiers. | `Run demist-ui on navigation and form controls` |
| **`token-harvest`** | Mines existing CSS tokens and colors into structured variables. | `Run token-harvest on <LEGACY_CSS>` |
| **`spec-generator`** | Auto-generates comprehensive DESIGN.md token ledgers. | `Run spec-generator to compile DESIGN.md` |
| **`viewport-conform`** | Multi-device responsiveness across desktop, tablet, and mobile. | `Run viewport-conform on <PAGE_LAYOUT>` |

---

### 5. Editorial Cadence & Layout Rhythm
| Discipline | Description | Exact Copy-Paste Prompt |
|:---|:---|:---|
| **`editorial-craft`** | Anti-slop landing page layout & strict 1-section-per-screen rule. | `Run editorial-craft on <LANDING_PAGE>` |
| **`prose-architecture`** | Writing declarative, authentic copy with zero marketing buzzwords. | `Run prose-architecture to rewrite copy in <PAGE>` |
| **`signature-interactions`**| Designing the 1–2 unforgettable interactive moments on a page. | `Run signature-interactions for <PRODUCT_HERO>` |
| **`finish-standards`** | Mandatory pre-flight quality gate before shipping UI. | `Run finish-standards audit on <PRODUCTION_PAGE>` |
| **`surface-containers`** | Layer elevations, border luminance, and container rhythm. | `Run surface-containers on card layouts` |
| **`backdrop-textures`** | Ambient gradients, subtle grain, and canvas background styling. | `Run backdrop-textures on background canvas` |
| **`section-catalog`** | Curated production patterns for headers, feature grids, and tables. | `Run section-catalog to scaffold <PAGE_SECTIONS>` |

---

### 6. Aesthetic Sanitization & De-Templating
| Discipline | Description | Exact Copy-Paste Prompt |
|:---|:---|:---|
| **`de-generic`** | Core engine for stripping away synthetic AI patterns and templates. | `Run de-generic on <AI_GENERATED_PAGE>` |
| **`filter-artifacts`** | Eliminating purple gradient halos, glow blobs, and blurry glassmorphism. | `Run filter-artifacts on <STYLES>` |
| **`hallmark-smells`** | Instant visual tells that give away uncurated AI code. | `Run hallmark-smells to audit <PAGE_SOURCE>` |
| **`aesthetic-remediation`**| Step-by-step before-and-after surgery on template-ridden UI. | `Run aesthetic-remediation on <GENERIC_CARDS>` |
| **`sanitized-tokens`** | Replacing random arbitrary hex values with semantic tokens. | `Run sanitized-tokens to clean color tokens` |

---

## Step-by-Step Walkthroughs

### How to Use OpusForge for a Single Component
Suppose you have a component `src/components/PricingCard.tsx` that feels generic, lacks tactile click feedback, and breaks when user plan names are long.

1. **Step 1: Sanitize AI cliches**
   > *"Run de-generic on `src/components/PricingCard.tsx`. Remove any neon gradient border or glassmorphic blur. Make borders 1px subtle neutral and background solid card surface."*

2. **Step 2: Add tactile click depth**
   > *"Run tactile-craft-engineering on the CTA button in `src/components/PricingCard.tsx`. Add active press scale(0.98), instant 0ms touch feedback, and high-visibility focus rings."*

3. **Step 3: Stress-test edge cases**
   > *"Run chaos-ui-tester on `src/components/PricingCard.tsx` with plan names of 60 characters and 10 features with long descriptions. Ensure no text clipping or button squishing."*

Your component is now production-hardened in under 3 minutes.

---

### How to Use OpusForge for a Complete Website
Suppose you want to launch a flagship product website.

1. **Step 1: Open chat in your project repository.**
2. **Step 2: Paste this exact instruction:**
   > *"opus-pipeline full-build for https://www.figma.com/design/:fileKey/:fileName?node-id=1:675*  
   > *Execute all 6 stages sequentially with verification gates:*  
   > *1. Token Intake: Extract layout, colors, and motion parameters into tokens.css.*  
   > *2. UX Blueprint: Mode Persuade (Editorial), equal left/right margins, container bounds.*  
   > *3. Editorial Craft: One section per screen at 1440x900, zero corporate buzzwords, 1 signature moment.*  
   > *4. Kinetic Polish: Composite-only spring curves, active press feedback, prefers-reduced-motion.*  
   > *5. Fortify: Skeleton loaders, empty states, chaos test with long strings, WCAG AA.*  
   > *6. De-Generic: Zero AI gradient blobs, bespoke human craft styling.*  
   > *Verify each gate before moving to the next."*
3. **Step 3: OpusForge executes autonomously**, reporting verification evidence at each gate.

---

## Repository Architecture

```text
opus-forge/
├── ATTRIBUTION.md                     # Upstream open-source credits & third-party notices
├── LICENSE                            # MIT License (Ganesh Yandigeri, 2026)
├── CONTRIBUTING.md                    # Engineering axioms & PR criteria
├── DISCIPLINES-CATALOG.md             # Complete guide for standalone component mode
├── rename-map.md                      # Single source of truth architectural translation ledger
├── inventory.md                       # Recursive baseline crawl across source repositories
├── progress.md                        # Transparent transformation log and verification checks
├── VERIFICATION-REPORT.md             # Certified 0-hit sanitization & parity audit
├── assets/                            # Architecture diagrams, screenshots, and visual assets
└── disciplines/
    ├── opus-pipeline/                 # Sovereign 6-Stage Master Build Engine (SKILL.md)
    ├── figma-conduit/                 # Live token extraction & frame inspection (SETUP.md)
    ├── structural-rigor/              # UX topology, surface modes, and fortification (45+ playbooks)
    ├── kinetic-physics/               # Tactile motion, spring curves, and 60fps budgets (20 skills)
    ├── editorial-cadence/             # Visual rhythm, bespoke copy, and moment design (22 playbooks + 1,594 assets)
    └── aesthetic-sanitizer/           # Anti-template heuristics and de-slop surgery (7 playbooks)
```

---

## Credits & Upstream Attribution

OpusForge is an integrated derivative work standing on the shoulders of giants in the open-source design engineering community. All original methodologies, motion physics, layout philosophies, and de-templating heuristics have been reworded, restructured, and attributed in full compliance with their respective open-source licenses (MIT, Apache 2.0, and CC BY 4.0).

👉 **For complete creator attributions, source repository links, license texts, and third-party notices, please see [ATTRIBUTION.md](ATTRIBUTION.md).**
