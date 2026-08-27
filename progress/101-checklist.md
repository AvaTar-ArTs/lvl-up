# 101 Progress Checklist

Use this as the human-readable launch checklist before advancing deeply into the Level 0–5 tracks.

The goal is not 100% memorization. Check an item when you can *do* it without blindly copying a tutorial.

## Foundations 101

- [ ] Navigate projects confidently from the terminal.
- [ ] Explain absolute vs relative paths.
- [ ] Create a Git branch and commit a meaningful checkpoint.
- [ ] Explain dependency/build tooling at a high level.
- [ ] Read/write a JSON document.
- [ ] Explain process boundaries and stdout/stderr.
- [ ] Explain request → response for an HTTP API.
- [ ] Reproduce and shrink a bug before attempting a fix.
- [ ] Measure before claiming a performance problem.

Guide: [Foundations 101](../101/foundations.md)

## Python 101

- [ ] Create and activate an isolated environment.
- [ ] Read/write files with `pathlib`.
- [ ] Parse/emit JSON.
- [ ] Break logic into functions/modules.
- [ ] Surface meaningful exceptions instead of hiding them.
- [ ] Build the Workflow Manifest Inspector mini-project.
- [ ] Explain which parts of the stack should remain Python.

Guide: [Python 101](../101/python.md)

## TypeScript 101

- [ ] Create and run a strict TypeScript project.
- [ ] Model data with interfaces/types/unions.
- [ ] Use narrowing rather than broad casts.
- [ ] Explain compile-time typing vs runtime validation.
- [ ] Use `async`/`await` with explicit failure handling.
- [ ] Build the Typed Workflow Viewer mini-project.
- [ ] Explain Node vs browser execution.

Guide: [TypeScript 101](../101/typescript.md)

## Rust 101

- [ ] Create/run/test a Cargo project.
- [ ] Explain ownership and borrowing practically.
- [ ] Use structs, enums, `Option`, and `Result`.
- [ ] Handle expected failures without `panic!`/blind `unwrap()`.
- [ ] Build a release binary.
- [ ] Build the Fast File Counter mini-project.
- [ ] Compare one Rust workload with an equivalent Python workload.

Guide: [Rust 101](../101/rust.md)

## C++ / Unreal 101

- [ ] Compile a tiny C++ program.
- [ ] Explain values, references, pointers, and lifetime.
- [ ] Explain stack vs heap at a practical level.
- [ ] Create a C++ Unreal Actor.
- [ ] Expose a property to the Unreal Editor.
- [ ] Build a reusable interaction component.
- [ ] Explain C++ vs Blueprint vs Python responsibilities.

Guide: [C++ / Unreal 101](../101/cpp-unreal.md)

## GPU / Shaders 101

- [ ] Explain CPU vs GPU responsibilities.
- [ ] Explain vertex and fragment stages.
- [ ] Explain UV coordinates.
- [ ] Modify a shader intentionally rather than by trial alone.
- [ ] Send a time/mouse parameter into a shader.
- [ ] Build the Procedural Signal Card mini-project.
- [ ] Measure frame time for the result.

Guide: [GPU / Shaders 101](../101/gpu-shaders.md)

## Swift 101

- [ ] Run a Swift program or package.
- [ ] Use structs/enums/optionals.
- [ ] Decode JSON using `Codable`.
- [ ] Build a small SwiftUI hierarchy.
- [ ] Explain state-driven UI.
- [ ] Build the Workflow Status Dashboard mini-project.
- [ ] Describe a clean Swift ↔ Python/Rust boundary.

Guide: [Swift 101](../101/swift.md)

## Integration 101

- [ ] Choose between file, subprocess, HTTP/socket, and FFI boundaries deliberately.
- [ ] Define request/output/error schemas before wiring layers together.
- [ ] Represent progress and cancellation explicitly.
- [ ] Keep machine output separate from human diagnostic output.
- [ ] Explain the cost of CPU ↔ GPU data movement.
- [ ] Build the Three-Layer Job mini-project or an equivalent boundary exercise.

Guide: [Integration 101](../101/integration.md)

## 101 Graduation

You have completed the 101 layer when you can draw your current stack and label *why* each language owns its layer.

```text
TypeScript → humans control/see
Python     → intelligence/orchestration
Rust       → native tooling
C++        → realtime runtime
GPU        → visual computation
Swift      → optional native Apple surface
```

Next: choose the first unfinished [full track](../README.md#what-to-learn-next) and build through its Level 0–5 ladder.
