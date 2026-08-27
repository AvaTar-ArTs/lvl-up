# GPU + Shader Programming Track

## Why This Track Matters

Shader programming is where programming becomes visual material. Instead of telling the CPU what every pixel should be, you write small programs that run massively in parallel on the GPU.

Use this track for:

- generative visuals
- realtime effects
- procedural textures
- cel/anime shading
- glitch systems
- particles
- lighting
- post-processing
- WebGPU experiences
- Unreal materials and custom HLSL

## Language Map

| Language | Best Habitat |
|---|---|
| GLSL | WebGL/OpenGL, Three.js shader work |
| WGSL | WebGPU |
| HLSL | DirectX-style pipelines, Unreal custom shader work |

Do not try to master all three at once. Learn the concepts once, then translate them between ecosystems.

## Level 0 — Orientation

Learn:

- CPU vs GPU execution
- vertices, fragments/pixels, textures, buffers
- shader stages
- normalized coordinates
- color spaces at a practical level
- why branching/data transfer can be expensive

Build:

- a fullscreen fragment shader that renders a gradient controlled by time and mouse position

Definition of done:

- understand what data enters the shader
- animate without CPU-side pixel loops

## Level 1 — GLSL With Purpose

Learn:

- vectors and matrices
- swizzling
- uniforms
- varying/interpolated values
- UV coordinates
- `smoothstep`, `mix`, `fract`, `mod`
- signed distance field basics
- noise concepts

Build:

**Procedural Signal Poster**

Create an animated visual containing:

- procedural shapes
- texture distortion
- animated color fields
- scanlines or halftone treatment
- mouse/audio-ready control parameters

Definition of done:

- no image texture required for the core visual
- effect scales with viewport size

## Level 2 — Three.js + Shader System

Learn:

- Three.js scene/camera/render loop
- ShaderMaterial
- render targets
- post-processing
- texture inputs
- instancing concepts

Build:

**Generative Character Aura System**

Create reusable visual effects around a 2D or 3D subject:

- energy field
- distortion
- particles
- color pulse
- outline/cel treatment

Expose parameters from TypeScript.

## Level 3 — WebGPU + WGSL

Learn:

- WebGPU pipeline concepts
- bind groups
- buffers
- compute shaders
- WGSL syntax
- GPU data flow

Build:

**GPU Particle Field**

Architecture:

```text
TypeScript control layer
          ↓
WebGPU buffers
          ↓
WGSL compute shader
          ↓
WGSL render shader
          ↓
100k+ particles / generative field
```

Definition of done:

- simulation state updates on GPU
- TypeScript controls parameters rather than individual particles

## Level 4 — HLSL + Unreal

Learn:

- Unreal material graph fundamentals
- material functions
- custom HLSL nodes where justified
- post-process materials
- depth, normals, masks
- performance implications of shader complexity

Build:

**Stylized World Shader Pack**

Include:

- cel/anime lighting
- ink outline or edge treatment
- hologram/glitch effect
- procedural emissive material
- post-process look

Definition of done:

- reusable parameterized materials
- shader complexity inspected and documented

## Level 5 — Capstone

Build **Generative Realtime World**.

Choose browser or Unreal as the primary runtime.

Required proof:

- procedural visual identity
- GPU-resident animation or simulation
- parameter controls from TypeScript or Unreal
- at least one custom shader authored from code rather than only node graphs
- measured frame performance
- graceful quality settings for weaker hardware

## Creative Effect Ideas

Use the track to explore:

- ink diffusion
- manga halftones
- neon edge extraction
- animated graffiti
- CRT/analog signal damage
- spectral ghosts
- heat haze
- liquid chrome
- procedural starfields
- music-reactive geometry
- dissolves
- portals
- stylized fire
- comic-panel transitions

## What To Combine It With

- TypeScript + WGSL → browser-based interactive art
- C++/Unreal + HLSL → game and cinematic worlds
- Python + shader generation → procedural parameter/content pipelines
