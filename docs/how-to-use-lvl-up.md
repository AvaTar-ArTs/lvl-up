# How To Use lvl-up

`lvl-up` works best as a build loop, not a reading list.

## The Weekly Loop

Use this cycle regardless of language:

### 1. Learn

Pick one concept that blocks the next feature.

Examples:

- TypeScript discriminated unions
- Rust ownership for filesystem records
- C++ references and object lifetime
- WGSL storage buffers
- Swift structured concurrency

Do not expand the week's curriculum just because adjacent topics look interesting.

### 2. Build

Use the concept immediately in a tiny feature or project slice.

The build should produce visible evidence: a CLI command, UI state, benchmark, shader, gameplay behavior, or native screen.

### 3. Integrate

Connect the new language to something already useful.

Examples:

- TypeScript UI launches Python.
- Rust scanner feeds Python.
- Python generates data consumed by Unreal C++.
- TypeScript modifies WGSL parameters.
- SwiftUI monitors a Python/Rust worker.

Integration is where knowledge becomes part of the stack instead of becoming trivia.

### 4. Measure

Choose evidence appropriate to the layer:

- UI: usability and failure behavior
- Rust: throughput, memory, binary size
- C++/Unreal: frame time, memory, Unreal Insights
- GPU: frame time, GPU load, shader complexity
- Swift: responsiveness, cancellation, native behavior

### 5. Ship

Create a reproducible result:

- tagged example
- packaged binary
- demo page
- packaged game build
- app bundle
- recorded benchmark

### 6. Review

Write five short answers:

1. What did this language make easier?
2. What became harder?
3. What belongs in this language now?
4. What should remain in Python or another layer?
5. What is the next capability bottleneck?

## Checkpoint Rules

Advance a level only when all three are true:

1. You can explain the important concept without copying a tutorial.
2. You have used it in a working artifact.
3. You can identify at least one case where you would *not* use it.

This prevents "tutorial completion" from masquerading as mastery.

## Recommended First 12 Build Sessions

### TypeScript block

1. Strict TypeScript CLI + typed workflow model.
2. Async filesystem/API exercise.
3. React UI over mocked workflow data.
4. Connect the UI to one Python process/API.
5. Add live progress and failure states.

### Rust block

6. Recursive file scanner.
7. Typed metadata + Result-based errors.
8. Hashing and duplicate detection.
9. Parallelize and benchmark.
10. Call the Rust tool from Python.

### Realtime preview

11. Unreal C++ Actor/Component exercise.
12. First shader: animated procedural fragment effect.

After session 12, choose whether to deepen Rust/product engineering or accelerate into C++/GPU based on what you most want to ship next.

## Progress State

`progress/roadmap.json` is intentionally machine-readable. Update each track's `status` as the learning sequence changes.

Suggested statuses:

- `next`
- `active`
- `queued`
- `paused`
- `complete`
- `optional`

A future dashboard or agent can read this file without scraping Markdown.

## Anti-Patterns

Avoid:

- learning three new languages simultaneously at beginner depth
- rewriting working Python without a measured reason
- using C++ for offline automation simply because it is lower-level
- introducing Rust when a 30-line Python script is already sufficient
- putting realtime gameplay loops in Python inside an engine that expects C++
- doing CPU pixel loops when a shader is the natural solution
- building a full web platform before proving the workflow it controls

## The Core Question

At every stage ask:

> What new capability am I buying with this complexity?

If the answer is unclear, keep the simpler layer.
