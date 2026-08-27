# Swift + SwiftUI Track

## Why Swift Is Optional but Powerful

Swift is not the next language to learn before TypeScript, Rust, or C++. It becomes valuable when you want your automation systems to feel like polished native Apple products.

Use it for:

- macOS control centers
- iPhone/iPad companion apps
- menu bar utilities
- native file pickers and system integration
- local notifications
- Apple platform UI
- Vision Pro experiments

Keep Python or Rust behind the app when they already own the heavy workflow.

## Level 0 — Orientation

Learn:

- Swift syntax basics
- Xcode project structure
- Swift Package Manager
- value vs reference types
- optionals
- SwiftUI view composition

Build:

- a tiny macOS dashboard displaying mocked workflow status cards

## Level 1 — State and Data Flow

Learn:

- structs/classes
- protocols
- enums
- async/await
- Codable
- Observation/SwiftUI state patterns
- navigation and commands

Build:

- a workflow model loaded from JSON with running/completed/failed states

Definition of done:

- UI state is derived from typed models rather than scattered booleans

## Level 2 — Native Project

Build **Creative Task Console**.

Features:

- browse workflow definitions
- launch local commands through an explicit process boundary
- show stdout/stderr
- open artifact folders
- persist recent runs

## Level 3 — Integration

Connect SwiftUI to either:

### Python service

```text
SwiftUI
  ↓
HTTP / local socket
  ↓
Python agents / pipelines
```

### Rust native service

```text
SwiftUI
  ↓
local process / FFI where justified
  ↓
Rust engine
```

Prefer a clean service/process boundary before reaching for complex FFI.

## Level 4 — Production Pattern

Learn:

- app lifecycle
- structured concurrency
- cancellation
- settings
- file coordination
- sandbox/permissions concepts
- logging
- packaging and signing concepts
- accessibility

Build:

- background task monitoring
- cancellation
- recent run history
- native notifications on completion/failure
- resilient reconnection if the backend restarts

## Level 5 — Capstone

Build **Native Creative Operations Console**.

Suggested interface:

```text
┌────────────────────────────────────┐
│ Creative Operations                │
├────────────────────────────────────┤
│ Agents         ● ready             │
│ Skills         214 indexed         │
│ Assets         18,431              │
│ Pipelines      12                  │
│                                    │
│ Active Runs                         │
│ trend-scan       ███████░ 72%      │
│ image-pipeline   complete ✓        │
│                                    │
│ [Generate] [Research] [Build]      │
└────────────────────────────────────┘
```

Proof of skill:

- native macOS application
- typed workflow/run models
- async backend communication
- cancellation and failure handling
- open generated artifacts from the native UI
- package a repeatable local setup

## When To Start

Start this track after a Python, TypeScript, or Rust workflow is valuable enough that a native Apple interface would improve how often and how comfortably you use it.
