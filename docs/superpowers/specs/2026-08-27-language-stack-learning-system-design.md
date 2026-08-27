# Language Stack Learning System Design

## Purpose

`lvl-up` is a practical learning system for expanding from Python-centered creative automation into full-stack product, systems, realtime, and GPU development.

The repository should answer four questions at all times:

1. What should I learn next?
2. Why does it matter to the systems I already build?
3. What should I build to prove I understand it?
4. What combination of languages unlocks the next capability tier?

## Core Stack

The recommended progression is:

1. **TypeScript** — product interfaces, browser apps, MCP clients/tools, web platforms, dashboards, Node services.
2. **Rust** — native tools, high-performance file/media engines, concurrency, distributable CLIs.
3. **C++ / Unreal Engine** — realtime engines, AAA/game technology, simulation, low-level performance.
4. **GPU programming** — GLSL, HLSL, WGSL, WebGPU, shaders, generative visuals, realtime rendering.
5. **Swift** — optional native Apple product layer for macOS/iOS/iPadOS/visionOS.

Python remains the orchestration and AI layer rather than being replaced.

## Learning Philosophy

Each track uses the same progression:

- **Level 0: Orientation** — understand the language's role and toolchain.
- **Level 1: Syntax with purpose** — learn only syntax needed to build something useful.
- **Level 2: Native project** — create a small standalone tool in the language.
- **Level 3: Integration** — connect the language to Python or another track.
- **Level 4: Production pattern** — packaging, testing, performance, observability, failure handling.
- **Level 5: Capstone** — ship a project that demonstrates why this language belongs in the stack.

## Architecture

The repository is documentation-first.

- `README.md` is the map and current recommended route.
- `tracks/` contains one focused curriculum per language/domain.
- `projects/` contains cross-language build challenges.
- `progress/roadmap.json` is a machine-readable representation of the progression and can later power a dashboard or automation.
- `docs/superpowers/` records design and implementation rationale.

No web framework, database, or CLI is introduced in the first version. Those become justified only when the learning content needs executable tracking or visualization.

## Track Boundaries

### TypeScript
Focus: productization of existing automation and AI systems.

### Rust
Focus: native acceleration, file/media processing, safe concurrency, binaries.

### C++ / Unreal
Focus: engine architecture, realtime systems, gameplay, rendering, console-class development concepts.

### GPU
Focus: programmable graphics, shaders, WebGPU, Unreal materials/HLSL, generative visual systems.

### Swift
Focus: native Apple control surfaces around AI/automation systems.

## Cross-Language Capstones

Capstones intentionally combine languages:

- TypeScript + Python: AI workflow control center.
- Rust + Python: native media/file indexing engine with Python orchestration.
- TypeScript + WGSL: realtime generative visual web experience.
- C++ + Unreal + Python + HLSL: procedural interactive world pipeline.
- Swift + Python/Rust: native macOS creative operations console.

## Success Criteria

The repository is successful when:

- The next language to learn is obvious.
- Every track has concrete projects instead of abstract exercises.
- Progress can be tracked without interpreting prose.
- Each project connects to real creative automation, AI, media, tooling, or game-development outcomes.
- The stack evolves from Python orchestration toward product, native systems, engines, and GPU execution without abandoning Python.
