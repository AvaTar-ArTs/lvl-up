# Rust 101

Rust is the native systems layer in `lvl-up`: fast binaries, safe concurrency, filesystem-heavy tooling, predictable memory behavior, and components that need to ship without a Python runtime.

## Why Rust Here

Use Rust when a measured workload wants:

- native performance;
- a single distributable executable;
- strong control over memory and ownership;
- safe concurrency;
- high-volume file or data processing.

Python should still orchestrate when it is the better glue.

## Toolchain

Verify:

```bash
rustc --version
cargo --version
```

Create a project:

```bash
cargo new rust-101
cd rust-101
cargo run
```

Useful commands:

```bash
cargo check
cargo test
cargo fmt --check
cargo clippy
cargo build --release
```

## Core Concepts

Focus on:

- immutable-by-default variables;
- ownership;
- borrowing and references;
- `String` vs `&str`;
- structs;
- enums;
- `Option<T>`;
- `Result<T, E>`;
- pattern matching;
- iterators;
- traits;
- the `?` operator;
- modules and crates.

## First Program

Replace `src/main.rs` with:

```rust
#[derive(Debug)]
struct Job {
    id: String,
    progress: f32,
}

fn summarize(job: &Job) -> String {
    format!("{}: {:.0}%", job.id, job.progress * 100.0)
}

fn main() {
    let job = Job {
        id: "render-001".to_string(),
        progress: 0.72,
    };

    println!("{}", summarize(&job));
}
```

Run:

```bash
cargo run
```

Notice that `summarize` borrows the job instead of taking ownership.

## Ownership In One Sentence

Rust asks you to make resource lifetime explicit enough that the compiler can prevent many memory and concurrency bugs before the program runs.

Do not try to memorize the borrow checker. Build small programs and let compiler messages teach you the constraints.

## Mini-Project: Fast File Counter

Build a CLI that:

1. accepts a directory;
2. walks it recursively;
3. counts files by extension;
4. totals bytes;
5. reports inaccessible paths without panicking;
6. emits JSON.

Then compare its release build with a Python equivalent on the same directory. The purpose is not to prove Rust always wins. The purpose is to learn how to measure when it earns its complexity.

## Mistakes To Avoid

- cloning values everywhere just to satisfy ownership errors;
- using `unwrap()` for expected failures;
- reaching for async before basic ownership is comfortable;
- optimizing before measuring;
- replacing simple Python glue with Rust;
- treating compiler errors as hostility instead of design feedback.

## Ready For The Full Track?

You are ready when you can:

- create/test/build a Cargo project;
- explain ownership and borrowing at a practical level;
- use structs/enums/`Result`;
- read a filesystem path;
- handle expected errors without panic;
- build a release binary;
- explain why one workload should or should not move out of Python.

Continue: [Rust Track](../tracks/rust.md)

Then build toward the **Native Asset Intelligence Engine**.
