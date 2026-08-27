# lvl-up 101 Onboarding Layer Design

## Purpose

Add a beginner-friendly entry layer in front of the existing Level 0–5 tracks without duplicating the deeper curriculum.

The repo currently explains *what to learn* and *what to build*. The 101 layer explains *how to start today*.

## Architecture

```text
README
  ↓
101/README.md
  ├── foundations.md
  ├── python.md
  ├── typescript.md
  ├── rust.md
  ├── cpp-unreal.md
  ├── gpu-shaders.md
  ├── swift.md
  └── integration.md
        ↓
tracks/*.md
        ↓
projects/capstones.md
```

## 101 Contract

Every language 101 answers the same questions:

1. What is this language/layer?
2. Why does it belong in this stack?
3. What should already be familiar?
4. What toolchain is required?
5. What are the smallest useful concepts?
6. What is the first runnable example?
7. What is the first mini-project?
8. What common mistakes should be avoided?
9. What proves readiness for the full track?
10. What should be opened next?

## Shared Foundations

`101/foundations.md` covers the transferable substrate: terminal literacy, Git, package/build systems, files/processes, JSON, HTTP, testing, debugging, profiling, environment variables, and reading documentation.

This prevents every language guide from re-teaching the same mechanics.

## Integration 101

`101/integration.md` teaches process/API boundaries and the principle that languages should cooperate through explicit contracts instead of being fused together unnecessarily.

## Progress

`progress/101-checklist.md` provides a human-readable completion checklist. Existing `progress/roadmap.json` remains the machine-readable macro roadmap.

## Constraints

- Python remains the orchestration center.
- 101s are launchpads, not encyclopedias.
- Examples must be immediately useful and small enough to type by hand.
- Every 101 links into its existing Level 0–5 track.
- Avoid arbitrary version pinning unless the repo later adds reproducible starter code.
- Learning remains project-first and capability-driven.
