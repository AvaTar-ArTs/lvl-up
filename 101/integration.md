# Integration 101

The real strength of `lvl-up` is not learning six languages. It is learning where each one stops.

A healthy multi-language system has explicit boundaries, stable contracts, and a reason for every layer.

## The Default Rule

Prefer the simplest boundary that works:

```text
file / JSON
    ↓
subprocess
    ↓
HTTP / WebSocket / socket
    ↓
FFI / native binding
```

Do not jump directly to FFI because it feels more advanced.

## Boundary 1: Files And JSON

Best for:

- offline pipelines;
- generated manifests;
- batch jobs;
- reproducible intermediate data.

Example:

```json
{
  "job_id": "scan-001",
  "input": "/assets",
  "status": "queued"
}
```

Strengths: inspectable, debuggable, language-neutral.

Weaknesses: slower for chatty realtime communication.

## Boundary 2: Subprocess + stdout

A powerful local pattern:

```text
Python orchestrator
      ↓ command
Rust executable
      ↓ JSONL events
Python
```

Rules:

- stdout should be machine-readable if another program consumes it;
- stderr should contain human/debug diagnostics;
- exit codes should mean something;
- cancellation and partial output need explicit behavior.

## Boundary 3: HTTP

Best when UI/services need a stable API.

```text
TypeScript browser
      ↓ HTTP
Python service
```

Define:

- request schema;
- response schema;
- error schema;
- authentication boundary;
- idempotency/retry behavior where relevant.

## Boundary 4: Streaming

Use Server-Sent Events, WebSockets, sockets, or structured stdout for long-running jobs.

A useful event model:

```json
{"type":"started","job_id":"render-001"}
{"type":"progress","job_id":"render-001","value":0.42}
{"type":"artifact","job_id":"render-001","path":"out/frame.png"}
{"type":"complete","job_id":"render-001"}
```

Typed events prevent interfaces from devolving into arbitrary log scraping.

## Boundary 5: Native Binding / FFI

Use when process overhead or API ergonomics genuinely matter.

Examples:

- Python ↔ Rust with PyO3/maturin;
- Swift ↔ native C-compatible interface;
- C++ calling C APIs;
- engine/plugin boundaries.

FFI introduces harder lifetime, ABI, packaging, and crash-boundary problems. Earn it with a measured need.

## GPU Boundary

GPU code is different.

```text
CPU language
  ↓ uniforms / buffers / textures
GPU shader
  ↓ rendered or computed output
```

The performance rule is often: move *systems of work* to the GPU, not individual tiny operations that constantly bounce data across the boundary.

## Canonical lvl-up Stack

```text
TypeScript
  product + interface
        ↓ API/events
Python
  intelligence + orchestration
   ┌────┴────┐
   ↓         ↓
 Rust       C++ / Unreal
 native     realtime runtime
 tooling       ↓
           GPU / shaders

Optional surface:
SwiftUI → API/process → Python/Rust
```

## Contract Checklist

Before connecting two layers, write down:

- Who owns the data?
- What is the input schema?
- What is the output schema?
- How are errors represented?
- How is cancellation represented?
- What happens if the producer crashes?
- What happens if the consumer restarts?
- Is the boundary synchronous or asynchronous?
- Is ordering guaranteed?
- Is the interface versioned?

## Mini-Project: Three-Layer Job

Build the same small workflow across three layers:

1. TypeScript creates a typed job request.
2. Python receives/orchestrates it.
3. Rust performs a filesystem-heavy operation and emits structured events.
4. Python forwards progress.
5. TypeScript displays state transitions.

Do not add a database, queue, container system, or FFI unless the mini-project proves it needs one.

## Graduation Test

You understand integration when you can defend this statement:

> “This boundary exists because these two layers have different responsibilities, and this contract lets either implementation evolve without leaking its internals into the other.”

Continue: [Cross-Stack Capstones](../projects/capstones.md)
