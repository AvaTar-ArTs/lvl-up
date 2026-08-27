# Rust Track

## Why Rust

Rust belongs in the stack when Python is excellent at orchestration but the underlying workload wants native performance, predictable memory use, safe concurrency, or a single distributable binary.

Use it for:

- high-volume file scanning
- hashing and deduplication
- media metadata extraction
- concurrent pipelines
- CLIs
- local daemons
- native libraries called from Python
- performance-sensitive infrastructure

## Level 0 — Orientation

Learn:

- Cargo
- crates and modules
- `cargo run`, `cargo test`, `cargo build --release`
- `rustfmt` and Clippy

Build:

- a CLI that recursively counts files by extension and prints totals

Definition of done:

- clean build
- formatted code
- Clippy produces no unexplained warnings

## Level 1 — Syntax With Purpose

Learn:

- ownership and borrowing
- references
- `String` vs `&str`
- structs and enums
- `Option` and `Result`
- pattern matching
- iterators
- traits
- error propagation with `?`

Build:

- a typed file-record parser that converts filesystem metadata into domain objects and reports recoverable errors

Definition of done:

- no panic for expected filesystem errors
- domain state modeled with enums/structs rather than stringly-typed values

## Level 2 — Native Project

Build **Fast Asset Scanner**.

Capabilities:

- recursive traversal
- extension/type classification
- file size aggregation
- hashing
- duplicate grouping
- JSON or JSONL export

Learn:

- `Path` / `PathBuf`
- buffered IO
- serialization with Serde
- ergonomic CLI design
- integration tests

Definition of done:

- handles inaccessible files without aborting the scan
- produces deterministic machine-readable output
- includes a release binary

## Level 3 — Integration

Learn two integration patterns:

### Pattern A: subprocess boundary

```text
Python
  ↓
Rust CLI
  ↓
JSONL
  ↓
Python
```

### Pattern B: native Python extension

Use PyO3/maturin when call overhead, deployment model, or API ergonomics justify it.

Build:

- connect the Fast Asset Scanner to a Python orchestration script
- compare CLI-boundary vs native-extension tradeoffs

## Level 4 — Production Pattern

Learn:

- Rayon or Tokio where appropriate
- bounded concurrency
- channels
- structured logging/tracing
- benchmarking
- profiling
- cancellation
- stable error types
- cross-platform release builds

Build:

**Asset Intelligence Engine**

Add:

- parallel scanning
- incremental indexing
- configurable hashing
- resumable runs
- progress events
- benchmark suite

Definition of done:

- benchmark against a Python baseline on the same dataset
- document where Rust wins and where Python remains simpler
- cancellation cannot corrupt output state

## Level 5 — Capstone

Build **Native Asset Intelligence Engine**.

Architecture:

```text
Python orchestration
        ↓
Rust engine
├── scan
├── hash
├── classify
├── dedupe
├── metadata
└── event stream
        ↓
JSONL / bindings
        ↓
TypeScript or Python UI
```

Proof of skill:

- process a realistically large asset tree
- benchmark throughput and memory use
- package a native binary
- integrate results back into a Python workflow
- demonstrate recoverable error handling and cancellation

## What To Learn After This

Move to [C++ + Unreal](cpp-unreal.md) when the goal shifts from tooling and infrastructure to realtime worlds, game engines, simulation, rendering, or engine-level creative technology.
