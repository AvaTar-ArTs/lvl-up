# Swift 101

Swift is the native Apple product layer in `lvl-up`. It becomes valuable when an existing workflow deserves a polished macOS, iPhone, iPad, or visionOS front end.

## Why Swift Is Later In The Route

Swift is not replacing Python, TypeScript, or Rust. It is the layer that makes a mature system feel native on Apple platforms.

```text
SwiftUI
  ↓
local API / process boundary
  ↓
Python orchestration or Rust engine
```

## Toolchain

Use Xcode for Apple apps and Swift Package Manager for package-oriented Swift work.

At the command line, verify:

```bash
swift --version
```

Create a small package if you want to learn language syntax outside Xcode:

```bash
mkdir swift-101 && cd swift-101
swift package init --type executable
swift run
```

## Core Concepts

Learn:

- `let` vs `var`;
- structs and classes;
- value vs reference semantics;
- optionals;
- enums;
- protocols;
- functions and closures;
- `Codable`;
- error handling;
- `async`/`await`;
- SwiftUI view composition;
- state and data flow.

## First Language Program

```swift
struct Job: Codable {
    let id: String
    let progress: Double
}

func summarize(_ job: Job) -> String {
    "\(job.id): \(Int(job.progress * 100))%"
}

let job = Job(id: "render-001", progress: 0.72)
print(summarize(job))
```

## First SwiftUI Mental Model

A SwiftUI view is a description of UI derived from state.

```swift
import SwiftUI

struct ContentView: View {
    let progress = 0.72

    var body: some View {
        VStack {
            Text("render-001")
            ProgressView(value: progress)
        }
        .padding()
    }
}
```

The important idea is not memorizing modifiers. It is learning that state should drive presentation predictably.

## Mini-Project: Workflow Status Dashboard

Create a macOS SwiftUI app that:

1. loads mocked jobs from JSON;
2. displays queued/running/complete/failed states;
3. shows progress;
4. filters by status;
5. opens a details view;
6. clearly displays malformed-data errors.

Do not connect a real backend yet. First prove the native data and UI model.

## Next Integration Step

Once the local model works, replace mocked JSON with a clean boundary:

- HTTP to a Python service;
- local socket;
- subprocess protocol;
- Rust service/binary.

Prefer a simple process or service boundary before complex FFI.

## Mistakes To Avoid

- scattering unrelated booleans through views instead of modeling state;
- blocking the main UI thread;
- mixing backend orchestration directly into every view;
- using FFI when a local process/API boundary is sufficient;
- building a native shell around a workflow that has not yet proven useful;
- ignoring accessibility and platform conventions.

## Ready For The Full Track?

You are ready when you can:

- build/run a Swift program;
- model data with structs/enums/optionals;
- decode JSON with `Codable`;
- build a small SwiftUI view hierarchy;
- explain state-driven UI;
- perform one async operation conceptually;
- describe how the app should communicate with Python or Rust.

Continue: [Swift + SwiftUI Track](../tracks/swift.md)

Use it when the stack deserves a native cockpit, not merely because a native app sounds impressive.
