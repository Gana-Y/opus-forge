# Contributing to OpusForge

We welcome contributions to **OpusForge** (`opus-forge`). Whether you are adding a new interaction discipline, refining a motion spring formula, or enhancing the defensive fortification test suite, please adhere to our architectural standards.

---

## 1. Core Engineering Axioms

1. **Physical Accuracy:** Every animation curve, spring constant (mass, stiffness, damping), and duration must be mathematically sound. Never invent arbitrary cubic beziers without physical intent.
2. **Composite Layer Only:** Motion must never trigger layout thrashing or browser repaints. Animate exclusively on `transform` and `opacity`.
3. **Zero AI Slop:** Reject purple gradients, blurry neon halos, centered emoji badges, and generic 3-box feature grids.
4. **Defensive Rigor:** No component is finished until it cleanly handles 0 items, 250+ character strings, and network drops without visual clipping.
5. **Accessibility as a Foundation:** Keyboard focus states (`:focus-visible`), ARIA landmarks, and `@media (prefers-reduced-motion: reduce)` overrides are non-negotiable.

---

## 2. Directory Conventions

- Core disciplines reside in `disciplines/`:
  - `disciplines/kinetic-physics/`: Spring dynamics, gesture manipulation, and micro-physics.
  - `disciplines/structural-rigor/`: Information topology, surface modes, and layout geometry.
  - `disciplines/editorial-cadence/`: Editorial design, section rhythm, and bespoke copywriting.
  - `disciplines/aesthetic-sanitizer/`: Anti-template rules and visual de-slop heuristics.
  - `disciplines/figma-conduit/`: Live token extraction and frame inspection bridges.
  - `disciplines/opus-pipeline/`: The master 6-stage autonomous build pipeline.

---

## 3. Pull Request Guidelines

1. **Parity Check:** Ensure modifications preserve functional equivalence and do not introduce broken cross-references.
2. **Test Coverage:** If introducing a new component, include test cases with `chaos-ui-tester` edge-case data.
3. **Licensing & Attribution:** If porting or adapting open-source work, ensure compatible permissive licensing (MIT, Apache 2.0, BSD) and document attribution in `ATTRIBUTION.md`.
