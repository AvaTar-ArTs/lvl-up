# Python Leverage

## Python Is Still The Center

Learning new languages should expand the stack, not create a ritual migration away from Python.

Keep Python where it is already excellent:

- AI and machine learning
- agents and orchestration
- automation
- research systems
- data transformation
- media pipelines
- Blender/DCC scripting
- prototyping
- glue between tools
- experimentation
- API services where extreme throughput is not the constraint

The question is not "Can Python do this?" It usually can. The question is whether another language offers a meaningful advantage for this particular layer.

## Decision Matrix

| Need | Default Choice | Why |
|---|---|---|
| AI agents, ML, research automation | Python | Ecosystem and iteration speed |
| Workflow orchestration | Python | Excellent glue and integration |
| Interactive web product | TypeScript | Browser-native, typed UI ecosystem |
| Node/MCP/web tooling | TypeScript | Native fit for JS/TS ecosystems |
| High-volume filesystem work | Rust | Native speed, safe concurrency, binaries |
| Distributable native CLI | Rust | Strong packaging and runtime footprint |
| Realtime game runtime | C++ | Engine ecosystem and performance control |
| Unreal gameplay systems | C++ + Blueprints | Native Unreal architecture |
| Offline Unreal asset automation | Python | Scripting and content-pipeline fit |
| Browser shaders | GLSL/WGSL | Direct GPU execution |
| Unreal shader/material code | HLSL/material graph | GPU-native rendering layer |
| Native Apple UI | Swift | Best platform integration |
| Database querying | SQL | Purpose-built data language |

## Migration Triggers

Consider moving a component out of Python when one or more of these are measured problems:

1. CPU throughput is insufficient.
2. Startup/runtime dependencies make distribution painful.
3. High concurrency becomes difficult to reason about.
4. The component belongs directly in a browser/UI ecosystem.
5. The component must run inside an engine/runtime that expects another language.
6. GPU execution is the actual solution.
7. Native platform integration is the product requirement.

Do not migrate merely because another language sounds more advanced.

## Hybrid Patterns

### Python + TypeScript

```text
TypeScript product/UI
        ↓
API / MCP / WebSocket
        ↓
Python intelligence
```

Best for AI products, creator tools, dashboards, and workflow systems.

### Python + Rust

```text
Python orchestrator
        ↓
Rust native worker
        ↓
heavy file/media/data work
```

Best for scanners, dedupe engines, indexing, transforms, and native CLIs.

### Python + C++/Unreal

```text
Python offline pipeline
        ↓
assets / data / generated content
        ↓
C++ realtime runtime
```

Best for games, simulation, procedural worlds, and realtime experiences.

### Python + GPU

```text
Python generates/configures
        ↓
shader parameters/data
        ↓
GPU executes visual computation
```

Best for generative visual systems and accelerated computation.

### Swift + Python/Rust

```text
SwiftUI native interface
        ↓
local API/process boundary
        ↓
Python or Rust backend
```

Best for a polished personal creative operations application on macOS.

## Rule Of Thumb

Use Python to decide **what should happen**.

Use TypeScript to let humans **control and see it**.

Use Rust to make native tooling **fast, safe, and distributable**.

Use C++ to make realtime systems **run the world**.

Use shaders to tell the GPU **how the world looks and moves**.

Use Swift when Apple devices should make the whole system **feel native**.
