# Language Stack Learning System Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a practical language-learning roadmap that extends Python-centered creative automation into product, native systems, realtime engines, and GPU programming.

**Architecture:** Keep the first release documentation-first. The root README explains the strategy, focused Markdown tracks teach each language through useful projects, a projects catalog connects multiple languages, and `progress/roadmap.json` provides machine-readable state for later dashboards or automations.

**Tech Stack:** Markdown, JSON; curricula covering Python, TypeScript, Rust, C++, Unreal Engine, GLSL/HLSL/WGSL/WebGPU, and Swift.

**Spec:** `docs/superpowers/specs/2026-08-27-language-stack-learning-system-design.md`

## Global Constraints

- Python remains the orchestration and AI layer rather than being replaced.
- Recommended progression: TypeScript → Rust → C++/Unreal → GPU programming, with Swift as an optional native Apple track.
- Every track must culminate in a concrete build connected to creative automation, AI, media, tooling, or game development.
- The first release introduces no unnecessary framework, database, or application runtime.

---

### Task 1: Repository map and progression model

**Files:**
- Create: `README.md`
- Create: `progress/roadmap.json`

**Interfaces:**
- Consumes: design spec.
- Produces: canonical progression ordering and stable track IDs used by all curriculum files.

- [ ] Write the root README with the stack map, recommended order, learning philosophy, and links to every track/project.
- [ ] Create valid JSON containing track IDs, priorities, levels, outcomes, and capstone IDs.
- [ ] Verify the JSON parses with `python -m json.tool progress/roadmap.json`.
- [ ] Commit with `docs: add lvl-up roadmap foundation`.

### Task 2: Product and systems tracks

**Files:**
- Create: `tracks/typescript.md`
- Create: `tracks/rust.md`

**Interfaces:**
- Consumes: track IDs `typescript` and `rust` from `progress/roadmap.json`.
- Produces: staged curricula and capstone requirements.

- [ ] Add TypeScript curriculum covering TypeScript, Node, React/Next concepts, async APIs, WebSockets, browser APIs, workers, testing, and integration with Python.
- [ ] Add Rust curriculum covering ownership, errors, iterators, traits, concurrency, CLI packaging, filesystem/media workloads, Python bindings, and benchmarking.
- [ ] Ensure each level includes a build and a definition of done.
- [ ] Commit with `docs: add typescript and rust learning tracks`.

### Task 3: Realtime and graphics tracks

**Files:**
- Create: `tracks/cpp-unreal.md`
- Create: `tracks/gpu-shaders.md`

**Interfaces:**
- Consumes: track IDs `cpp-unreal` and `gpu-shaders`.
- Produces: game/engine and graphics learning paths.

- [ ] Add C++/Unreal curriculum from core C++/RAII through Unreal gameplay architecture, profiling, rendering, and Python-assisted asset pipelines.
- [ ] Add GPU curriculum spanning shader fundamentals, GLSL, WebGL/Three.js, WGSL/WebGPU, HLSL/Unreal, procedural effects, and optimization.
- [ ] Explicitly distinguish runtime code, tooling code, and GPU code.
- [ ] Commit with `docs: add realtime and gpu learning tracks`.

### Task 4: Native Apple track and language combinations

**Files:**
- Create: `tracks/swift.md`
- Create: `projects/capstones.md`

**Interfaces:**
- Consumes: all track IDs.
- Produces: optional Apple-native path plus integration challenges.

- [ ] Add Swift/SwiftUI curriculum centered on native control surfaces for automation systems.
- [ ] Add five cross-language capstones with architecture, milestone sequence, and proof-of-skill criteria.
- [ ] Include at least one game/realtime capstone and one native desktop capstone.
- [ ] Commit with `docs: add swift track and cross-stack capstones`.

### Task 5: Existing Python leverage and operating guide

**Files:**
- Create: `tracks/python-leverage.md`
- Create: `docs/how-to-use-lvl-up.md`

**Interfaces:**
- Consumes: complete roadmap.
- Produces: rules for deciding what stays in Python versus moves to another language.

- [ ] Document Python's continuing roles: AI, agents, orchestration, automation, data, asset pipelines, Blender/media tooling, prototyping.
- [ ] Add a decision matrix for Python vs TypeScript vs Rust vs C++ vs shaders vs Swift.
- [ ] Document a weekly learn/build/integrate/review loop and checkpoint rules.
- [ ] Commit with `docs: add python leverage and operating guide`.

### Task 6: Verification

**Files:**
- Verify all files created by Tasks 1–5.

**Interfaces:**
- Consumes: complete documentation tree.
- Produces: a coherent, navigable v1.

- [ ] Parse `progress/roadmap.json`.
- [ ] Check every README link resolves to an existing path.
- [ ] Search for `TBD`, `TODO`, and unfinished placeholders; remove any accidental placeholders.
- [ ] Confirm every roadmap track has a matching curriculum file.
- [ ] Commit any corrections with `docs: verify lvl-up learning system`.
