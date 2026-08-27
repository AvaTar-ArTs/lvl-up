# lvl-up

A practical learning system for expanding a Python-centered creative automation stack into product engineering, native systems, realtime engines, and GPU programming.

This repository is not a generic programming curriculum. It is a **capability ladder**: learn a language when it unlocks something useful, then prove it by building.

## Start Here — The 101 Layer

New to one of the languages or systems? Start with the [lvl-up 101 index](101/README.md).

The 101 layer is designed to get you from orientation to a runnable mini-project quickly, then hand you into the deeper Level 0–5 tracks.

```text
Foundations 101
      ↓
Python 101
      ↓
TypeScript 101
      ↓
Rust 101
      ↓
C++ / Unreal 101
      ↓
GPU / Shaders 101
      ↓
Swift 101 (optional)
      ↓
Integration 101
      ↓
Full Tracks → Capstones
```

Fast links: [Foundations](101/foundations.md) · [Python](101/python.md) · [TypeScript](101/typescript.md) · [Rust](101/rust.md) · [C++ / Unreal](101/cpp-unreal.md) · [GPU / Shaders](101/gpu-shaders.md) · [Swift](101/swift.md) · [Integration](101/integration.md) · [101 Checklist](progress/101-checklist.md)

## Recommended Stack

```text
                         PRODUCTS
                     TypeScript / TSX
                  web • apps • MCP • UI
                           │
                           ▼
                         PYTHON
                  AI • agents • automation
                media • research • pipelines
                           │
                 ┌─────────┴─────────┐
                 ▼                   ▼
               RUST                 C++
        native tools • speed     engines • realtime
        concurrency • binaries   Unreal • simulation
                 │                   │
                 └─────────┬─────────┘
                           ▼
                    GPU PROGRAMMING
                 GLSL • HLSL • WGSL
              WebGPU • shaders • rendering
                           │
                           ▼
                    CREATIVE COMPUTING

Optional native product surface: Swift / SwiftUI
```

## What To Learn Next

| Priority | Track | Why |
|---|---|---|
| 1 | [TypeScript](tracks/typescript.md) | Turn automation and AI systems into interactive products, dashboards, browser tools, MCP surfaces, and web platforms. |
| 2 | [Rust](tracks/rust.md) | Build fast native binaries, high-volume file/media engines, safe concurrent systems, and distributable CLIs. |
| 3 | [C++ + Unreal](tracks/cpp-unreal.md) | Enter realtime engines, AAA/game development, simulation, rendering, and low-level creative technology. |
| 4 | [GPU + Shaders](tracks/gpu-shaders.md) | Program the visual layer directly with GLSL, HLSL, WGSL, WebGPU, and realtime effects. |
| 5 | [Swift + SwiftUI](tracks/swift.md) | Build polished native macOS/iOS/iPadOS/visionOS control surfaces for the stack. |

Python remains central. See [Python Leverage](tracks/python-leverage.md) for what should stay in Python and when another language earns its place.

## Learning Model

Every track uses the same six levels.

| Level | Name | Goal |
|---|---|---|
| 0 | Orientation | Understand where the language belongs and install the toolchain. |
| 1 | Syntax With Purpose | Learn only the language concepts needed for a useful build. |
| 2 | Native Project | Build something standalone in that language. |
| 3 | Integration | Connect it to Python or another layer of the stack. |
| 4 | Production Pattern | Add testing, packaging, performance, observability, and failure handling. |
| 5 | Capstone | Ship something that proves why the language belongs in the ecosystem. |

The loop is simple:

```text
LEARN → BUILD → INTEGRATE → MEASURE → SHIP → REVIEW
```

Do not spend a month solving disconnected syntax puzzles if you can learn the same concepts while building a tool you actually want.

## Suggested Route

### Phase 1: Productize

Learn TypeScript deeply enough to put interfaces around existing Python systems.

Target stack:

```text
TypeScript / React / Next.js
          ↓
      API / MCP
          ↓
        Python
```

Exit condition: ship an interactive control surface that drives a real Python workflow.

### Phase 2: Native Acceleration

Move one CPU-heavy or filesystem-heavy component into Rust.

```text
Python orchestrator
       ↓
Rust native engine
       ↓
files • metadata • hashing • media
```

Exit condition: benchmark the Rust implementation, package it as a binary or Python extension, and demonstrate a meaningful operational advantage.

### Phase 3: Realtime Worlds

Learn C++ through Unreal instead of treating C++ as an abstract academic subject.

```text
Unreal
├── C++ gameplay/runtime
├── Blueprints rapid composition
├── Python asset automation
└── HLSL/material shaders
```

Exit condition: ship a small interactive world containing a custom C++ gameplay system and a Python-assisted content pipeline.

### Phase 4: Program The GPU

Use shaders to bridge coding and visual design.

Target progression:

```text
Three.js → GLSL → WebGPU → WGSL → HLSL / Unreal
```

Exit condition: create a realtime generative visual system that would be impractical as CPU-side pixel manipulation.

### Phase 5: Native Creative OS

Optional but high-value on Apple platforms: wrap automation systems in SwiftUI.

Exit condition: build a native macOS control center that launches, monitors, or visualizes Python/Rust workflows.

## Capstones

The real graduation tests live in [Cross-Stack Capstones](projects/capstones.md):

1. Creative Workflow Control Center — TypeScript + Python
2. Native Asset Intelligence Engine — Rust + Python
3. Generative Realtime Web World — TypeScript + WebGPU/WGSL
4. Procedural Unreal Universe — C++ + Unreal + Python + HLSL
5. Native Creative Operations Console — Swift + Python/Rust

## Decision Rule

Before adding a language, ask:

> What capability does this language unlock that the current stack handles poorly?

If there is no strong answer, do not add it yet.

## Repository Map

```text
lvl-up/
├── README.md
├── 101/
│   ├── README.md
│   ├── foundations.md
│   ├── python.md
│   ├── typescript.md
│   ├── rust.md
│   ├── cpp-unreal.md
│   ├── gpu-shaders.md
│   ├── swift.md
│   └── integration.md
├── tracks/
│   ├── python-leverage.md
│   ├── typescript.md
│   ├── rust.md
│   ├── cpp-unreal.md
│   ├── gpu-shaders.md
│   └── swift.md
├── projects/
│   └── capstones.md
├── progress/
│   ├── roadmap.json
│   └── 101-checklist.md
└── docs/
    ├── how-to-use-lvl-up.md
    └── superpowers/
        ├── specs/
        └── plans/
```

## Start Here

If a layer is unfamiliar, begin with its [101 guide](101/README.md). If the fundamentals are already comfortable, start with [TypeScript](tracks/typescript.md) while continuing to build in Python.

The goal is not to replace your strongest layer. The goal is to surround it with better interfaces, faster machinery, realtime engines, and programmable graphics.
