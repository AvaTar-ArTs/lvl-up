# Cross-Stack Capstones

These projects are the graduation tests for `lvl-up`. Each one exists because the combination of languages is more capable than any one layer alone.

## 1. Creative Workflow Control Center

**Stack:** TypeScript + Python

**Goal:** Turn existing AI/automation workflows into an interactive product surface.

Architecture:

```text
Next.js / TypeScript
├── workflow catalog
├── run launcher
├── live logs
├── asset viewer
└── settings
        ↓
REST / WebSocket / MCP
        ↓
Python orchestration
├── agents
├── media pipelines
├── research
└── automation
```

Milestones:

1. Display static typed workflow definitions.
2. Launch one Python workflow.
3. Stream progress/logs.
4. Handle failure/cancellation.
5. Persist run history.
6. Package a repeatable local deployment.

Proof of skill:

- typed domain model
- async job lifecycle
- clean language boundary
- usable UI around a real workflow

---

## 2. Native Asset Intelligence Engine

**Stack:** Rust + Python

**Goal:** Accelerate high-volume asset/file intelligence while preserving Python as orchestration.

Architecture:

```text
Python command/orchestrator
          ↓
Rust scanner/indexer
├── walk
├── hash
├── classify
├── metadata
├── dedupe
└── progress events
          ↓
JSONL / Python binding
```

Milestones:

1. Recursive scanner.
2. Typed metadata records.
3. Hashing and duplicate groups.
4. Parallel processing.
5. Progress/cancellation.
6. Python integration.
7. Benchmark against equivalent Python workload.

Proof of skill:

- native binary
- safe concurrency
- measured performance
- recoverable errors
- useful Python integration

---

## 3. Generative Realtime Web World

**Stack:** TypeScript + WebGPU + WGSL

**Goal:** Build a browser experience where TypeScript orchestrates and the GPU performs the visual simulation.

Architecture:

```text
TypeScript UI/state
        ↓
WebGPU pipeline
├── buffers
├── textures
└── bind groups
        ↓
WGSL
├── compute
└── render
```

Milestones:

1. WebGPU initialization.
2. Typed shader parameter model.
3. GPU-driven particle/field simulation.
4. Interactive controls.
5. Audio or timeline modulation.
6. Performance/quality tiers.

Proof of skill:

- substantial simulation state remains GPU-side
- TypeScript controls systems rather than micromanaging particles
- measured frame performance
- distinctive procedural visual language

---

## 4. Procedural Unreal Universe

**Stack:** C++ + Unreal + Python + HLSL

**Goal:** Build a miniature end-to-end creative universe pipeline from generated content to realtime world.

Architecture:

```text
Python creation layer
├── narrative data
├── encounter definitions
├── asset metadata
└── batch tooling
        ↓
Unreal content pipeline
        ↓
C++ runtime
├── gameplay subsystem
├── reusable components
├── spawning/state
└── save/config
        ↓
HLSL / materials
└── stylized visual identity
```

Milestones:

1. C++ gameplay foundation.
2. Data-driven encounter system.
3. Python content generator/importer.
4. Reusable runtime components.
5. Custom stylized shader/material.
6. Profile one real bottleneck.
7. Package a desktop build.

Proof of skill:

- C++ owns realtime behavior
- Python owns offline automation
- shader code materially affects presentation
- content is data-driven rather than hardcoded into a single level

---

## 5. Native Creative Operations Console

**Stack:** Swift + Python and/or Rust

**Goal:** Build a polished native macOS front door for the broader creative stack.

Architecture:

```text
SwiftUI
├── agent status
├── pipeline launcher
├── run history
├── asset browser
└── notifications
        ↓
local API / process boundary
        ↓
Python orchestration
        ↓
optional Rust native engine
```

Milestones:

1. Typed workflow/run models.
2. Native dashboard.
3. Backend process communication.
4. Live progress.
5. Cancellation and recovery.
6. Artifact opening/reveal.
7. Native completion notifications.

Proof of skill:

- native macOS interaction model
- structured concurrency
- resilient backend communication
- useful integration with an existing workflow

---

# Final Boss: Creative Computing Platform

After the five capstones, combine the lessons rather than literally merging every project into one monolith.

```text
                     TYPESCRIPT
                  product surfaces
                        │
                        ▼
                      PYTHON
                AI + orchestration
                  ┌─────┴─────┐
                  ▼           ▼
                RUST         C++
             native tools   realtime
                  │           │
                  └─────┬─────┘
                        ▼
                 GPU / SHADERS
                        │
                        ▼
                    SWIFTUI
             optional native cockpit
```

The graduation criterion is architectural judgment: each language has a clear responsibility, cross-language boundaries are explicit, and no language is present merely because it is fashionable.
