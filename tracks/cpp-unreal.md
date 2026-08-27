# C++ + Unreal Engine Track

## Why C++ Through Unreal

C++ opens the engine/runtime layer: realtime simulation, gameplay systems, rendering architecture, performance-critical code, and the concepts behind console-class development.

Learn it through Unreal so each difficult concept has a concrete reason to exist.

Use it for:

- Unreal gameplay systems
- engine extensions
- simulation
- realtime media
- performance-critical runtime code
- lower-level graphics and systems work

Python remains useful for asset processing, content generation, Blender/DCC automation, build tooling, and offline pipelines.

## Level 0 — Orientation

Learn:

- compiler/build model
- headers vs implementation files
- Unreal project/module structure
- Unreal Editor, Build Tool, reflection macros, and generated code at a conceptual level
- Blueprints vs C++ responsibilities

Build:

- a tiny Unreal project with one C++ Actor exposed to Blueprints

Definition of done:

- compile from a clean project state
- place the Actor in a level
- modify a C++ property from the editor

## Level 1 — C++ With Purpose

Learn:

- values, references, pointers
- `const`
- classes and structs
- constructors/destructors
- RAII
- stack vs heap
- smart pointers in standard C++
- templates conceptually
- containers
- ownership and lifetime

Unreal-specific concepts:

- `UObject`
- `AActor`
- `UActorComponent`
- `APawn`
- `ACharacter`
- `AController`
- `AGameMode`
- `Subsystem`
- Unreal object references and garbage collection

Build:

- an interactable object system using an Actor Component and a small C++ interface

Definition of done:

- multiple Actors reuse the interaction behavior
- Blueprints can configure presentation without owning core runtime logic

## Level 2 — Native Realtime Project

Build **Procedural Encounter Sandbox**.

Features:

- player character
- spawn manager
- reusable encounter definitions
- health/damage component
- event-driven game state
- simple save/config data

Learn:

- composition over inheritance
- delegates/events
- data assets
- gameplay framework boundaries
- object lifetime
- debugging

## Level 3 — Python + Unreal Integration

Build an offline content pipeline:

```text
Python generator
      ↓
characters / encounters / metadata
      ↓
validated assets / JSON / import data
      ↓
Unreal Editor pipeline
      ↓
C++ runtime systems
```

Use Python for:

- content generation
- batch imports
- asset naming/validation
- metadata transformation
- procedural authoring support

Do not put frame-by-frame gameplay logic in Python.

## Level 4 — Production Pattern

Learn:

- profiling before optimization
- Unreal Insights
- threading concepts
- async tasks
- memory/lifetime debugging
- object pooling where justified
- data-oriented thinking
- network replication fundamentals
- build configurations
- plugin/module boundaries

Build:

- instrument the sandbox
- identify one measured bottleneck
- improve it without changing behavior
- document the before/after measurement

Definition of done:

- optimization is evidence-driven
- runtime systems have clear ownership
- failures and invalid content are surfaced during development rather than silently ignored

## Level 5 — Capstone

Build **Procedural Unreal Universe**.

Architecture:

```text
Python
├── narrative/content generation
├── asset metadata
└── offline automation
        ↓
Unreal Engine
├── C++ runtime architecture
├── Blueprints composition
├── animation / assets
└── HLSL/material shaders
        ↓
interactive realtime world
```

Required proof:

- custom C++ gameplay subsystem
- reusable components rather than one-off level logic
- Python-assisted content or asset pipeline
- custom material/shader work
- profiling capture and one documented optimization
- packaged desktop build

## PS5 Direction

C++/Unreal is the relevant learning direction for modern console-class game development. Actual PlayStation SDKs, platform documentation, packaging, certification, and hardware access require acceptance into Sony's PlayStation developer program. Treat the public learning goal as mastering engine/runtime principles and Unreal first; platform-specific work comes after authorized SDK access.

## What To Learn Alongside This

Study [GPU + Shaders](gpu-shaders.md) once you want to control how the world is rendered rather than only what the world does.
