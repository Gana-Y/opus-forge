# Figma Conduit: Live Token & Frame Inspection Protocol

The **Figma Conduit** serves as the live extraction bridge between design assets hosted in Figma and the OpusForge engineering pipeline. It enables autonomous extraction of design variables, typographic scales, color systems, spacing units, and motion parameters directly through the Model Context Protocol (MCP).

---

## 1. Architectural Role in OpusForge

Within the OpusForge flagship pipeline (`opus-pipeline`), the Figma Conduit acts as **Stage 1 (`token-intake`)**. It inspects target frames, extracts raw design tokens, and converts them into production-ready semantic variables before layout or component authoring begins.

```
┌─────────────────────────────────┐
│     Figma Design System / URL   │
└────────────────┬────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│       Figma Conduit (MCP)       │
│  - get_design_context           │
│  - get_motion_context           │
│  - get_variable_defs            │
└────────────────┬────────────────┘
                 │
                 ▼
┌─────────────────────────────────┐
│   OpusForge Semantic Tokens     │
│  - Spacing / Margin Geometry    │
│  - Typographic Scales & Weights │
│  - Semantic Chroma Tokens       │
│  - Motion & Spring Curves       │
└─────────────────────────────────┘
```

---

## 2. MCP Connection & Setup Guide

### Method A: Official Antigravity / Cursor / Claude Plugin
1. Open your workspace settings or plugin manager.
2. Locate the official Figma partner plugin:
   ```json
   {
     "mcpServers": {
       "figma": {
         "command": "npx",
         "args": ["-y", "@figma/mcp-server"]
       }
     }
   }
   ```
3. Authenticate with your Figma account via the OAuth handshake or provide your Personal Access Token (`FIGMA_PERSONAL_ACCESS_TOKEN`).

### Method B: Figma Desktop Live Bridge
1. Launch the Figma Desktop application.
2. Under **Settings > Developer Settings**, enable **Model Context Protocol Bridge**.
3. OpusForge automatically interfaces with the local bridge endpoint on port `3845` or via the standard MCP lazy-loaded registry.

---

## 3. Core Extraction Operations

### Operation 1: Inspecting Target Frames (`get_design_context`)
When provided with a Figma URL (e.g., `https://www.figma.com/design/:fileKey/:fileName?node-id=1:675`):
- Call `get_design_context` targeting the specified `node-id`.
- Extract container bounding dimensions, layout modes (Auto Layout horizontal/vertical), paddings, gap geometry, and corner radii.
- Map fill parameters: solid fills, radial/linear gradients, image fills, and background blurs.

### Operation 2: Extracting Kinetic Physics (`get_motion_context`)
- If the node contains prototype interactions, keyframes, or Smart Animate transitions:
- Call `get_motion_context` to capture spring parameters (mass, stiffness, damping) or cubic bezier curves (`cubic-bezier(x1, y1, x2, y2)`) and transition durations in milliseconds.
- Pass these directly into **Stage 4 (`kinetic-polish`)** for pixel-accurate physical recreation.

### Operation 3: Harvesting Global Design Tokens (`get_variable_defs`)
- Retrieve all defined Figma Variables across color collections, spacing modes, and typography aliases.
- Translate Figma variable collections into `tokens.css` or Tailwind configuration extensions.

---

## 4. Synthesis Rules for OpusForge

1. **Token Hierarchy:** Never hardcode extracted pixel or hex values into components. Always route them through OpusForge semantic variables (e.g., `--canvas-bg`, `--surface-card`, `--accent-primary`).
2. **Auto Layout to Flex/Grid:** Translate Figma Auto Layout properties (`flex-direction`, `justify-content`, `align-items`, `gap`) into modern CSS Flexbox and Grid primitives.
3. **Sub-pixel & Optical Correction:** Figma renders vector shapes using direct canvas drawing. Web DOM elements require optical corrections (e.g., border box sizing, text rendering smoothing `-webkit-font-smoothing: antialiased`).
4. **Fallback Handling:** If a live Figma URL is not provided in a build request, the pipeline falls back gracefully to Stage 2 (`blueprint`), querying the user's brief, target aesthetic, and existing project conventions.
