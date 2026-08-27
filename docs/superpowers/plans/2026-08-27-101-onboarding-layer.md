# 101 Onboarding Layer Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add a coherent 101 layer that gets a learner from orientation to the existing Level 0–5 tracks with minimal friction.

**Architecture:** A new `101/` directory contains one shared foundations guide, one guide per major stack layer, and one integration guide. The root README links to the 101 index, while the existing `tracks/` and `projects/` remain the deeper learning and graduation layers.

**Tech Stack:** Markdown, GitHub, shell commands, language-specific starter examples.

**Spec:** `docs/superpowers/specs/2026-08-27-101-onboarding-layer-design.md`

## Global Constraints

- Keep Python as the orchestration center.
- Keep 101s shorter and more actionable than full tracks.
- Every 101 must contain a first runnable example, first mini-project, mistakes, readiness criteria, and next link.
- Avoid unnecessary dependencies and version-specific churn.

---

### Task 1: Build the 101 navigation layer

**Files:**
- Create: `101/README.md`
- Create: `101/foundations.md`

- [ ] Add the 101 map and recommended order.
- [ ] Add transferable foundations and a readiness checklist.
- [ ] Verify all links resolve.

### Task 2: Build language 101s

**Files:**
- Create: `101/python.md`
- Create: `101/typescript.md`
- Create: `101/rust.md`
- Create: `101/cpp-unreal.md`
- Create: `101/gpu-shaders.md`
- Create: `101/swift.md`

- [ ] Use the common 101 contract from the spec.
- [ ] Include copyable first examples and mini-projects.
- [ ] Link each guide to the matching full track.

### Task 3: Build cross-language onboarding

**Files:**
- Create: `101/integration.md`
- Create: `progress/101-checklist.md`

- [ ] Teach process, API, file, and FFI boundaries.
- [ ] Add a practical completion checklist.

### Task 4: Connect the root README

**Files:**
- Modify: `README.md`

- [ ] Add a Start Here / 101 section near the top.
- [ ] Update the repository map.
- [ ] Preserve the existing capability ladder and capstones.

### Task 5: Verify

- [ ] Fetch the recursive tree and confirm every expected file exists.
- [ ] Search for placeholder markers such as `TODO`, `TBD`, and `FIXME`.
- [ ] Fetch `README.md` and `101/README.md` to confirm navigation.
