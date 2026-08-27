# TypeScript Track

## Why This Is First

TypeScript gives the fastest immediate leverage because it turns scripts, agents, pipelines, and APIs into products people can see and operate.

Use it for:

- React/Next.js interfaces
- dashboards and control panels
- browser extensions
- Node services
- WebSockets and realtime UI
- MCP clients and tool surfaces
- workflow editors
- creator platforms

Keep Python behind it when Python already owns the intelligence or automation.

## Level 0 — Orientation

Learn:

- TypeScript compiler and `tsconfig.json`
- Node.js runtime
- npm/pnpm package structure
- ESM modules
- basic browser vs server runtime differences

Build:

- a typed CLI that reads a JSON workflow manifest and prints a human-readable summary

Definition of done:

- strict TypeScript enabled
- no `any` required for core domain objects
- project builds and runs from a clean install

## Level 1 — Syntax With Purpose

Learn:

- primitives and unions
- interfaces vs type aliases
- generics
- narrowing
- discriminated unions
- async/await and Promises
- error handling
- modules

Build:

- a typed content-job model with states such as `queued`, `running`, `failed`, and `complete`
- a validator that rejects malformed job data

Definition of done:

- impossible job states are difficult to represent
- error cases are explicit

## Level 2 — Native Project

Learn:

- Node filesystem APIs
- fetch
- streams
- environment configuration
- basic testing
- CLI argument parsing

Build:

**Workflow Inspector**

A Node/TypeScript application that scans a folder of workflow JSON files, validates them, summarizes them, and exports an index.

Stretch goals:

- watch mode
- incremental re-indexing
- HTML report generation

## Level 3 — Integration

Learn:

- REST APIs
- Server-Sent Events
- WebSockets
- subprocess boundaries
- JSON schema
- MCP architecture concepts

Build:

**Python Pipeline Console**

```text
TypeScript UI
     ↓
Node / API layer
     ↓
Python worker
     ↓
creative pipeline
```

Required features:

- launch a Python task
- stream progress to the browser
- display logs
- surface success/failure cleanly
- inspect generated artifacts

## Level 4 — Production Pattern

Learn:

- React fundamentals
- Next.js application architecture
- state ownership
- server/client boundaries
- component testing
- API authentication concepts
- background-job architecture
- structured logging
- Web Workers

Build:

Upgrade the Pipeline Console into a small production-quality application.

Definition of done:

- failures produce actionable UI states
- long jobs do not freeze the interface
- typed boundaries exist between UI, API, and worker layers
- tests cover domain state transitions

## Level 5 — Capstone

Build **Creative Workflow Control Center**.

Features:

- visual workflow catalog
- agent/skill browser
- pipeline launcher
- run history
- live logs
- asset results panel
- configuration editor
- reusable typed API client

Architecture:

```text
React / Next.js / TypeScript
            ↓
        typed API
            ↓
   Python orchestration
            ↓
agents • media • research • automation
```

Proof of skill:

- demonstrate an end-to-end workflow launched from the browser
- show typed runtime state transitions
- recover gracefully from a worker failure
- package setup so another machine can run it

## What To Learn After This

Move to [Rust](rust.md) when you find a component that is slow, concurrency-heavy, filesystem-heavy, or awkward to distribute as Python.
