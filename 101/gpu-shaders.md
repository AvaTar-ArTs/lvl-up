# GPU / Shaders 101

Shaders are tiny programs executed massively in parallel on the GPU. In `lvl-up`, this is where code becomes visual material: procedural imagery, realtime effects, particles, lighting, post-processing, and generative worlds.

## The Mental Model

CPU code usually orchestrates.

GPU code usually performs the same kind of operation across huge amounts of data in parallel.

```text
TypeScript / C++
    ↓ parameters + buffers
GPU pipeline
    ↓
shader program
    ↓
pixels / vertices / compute results
```

## The Three Languages In This Track

| Language | Where to start using it |
|---|---|
| GLSL | WebGL / Three.js |
| WGSL | WebGPU |
| HLSL | Unreal / DirectX-style pipelines |

Learn graphics concepts once. Translate syntax later.

## Core Concepts

Understand:

- vertex vs fragment/pixel work;
- coordinates and UVs;
- vectors;
- color as numeric data;
- uniforms/parameters;
- interpolation;
- textures;
- buffers;
- render loop/time;
- `mix`, `smoothstep`, `fract`, `mod` style operations;
- why moving data between CPU and GPU can be expensive.

## First Fragment Shader

Conceptual GLSL fragment shader:

```glsl
uniform float uTime;
varying vec2 vUv;

void main() {
    vec3 a = vec3(0.1, 0.2, 0.8);
    vec3 b = vec3(0.9, 0.1, 0.5);
    float wave = 0.5 + 0.5 * sin(uTime + vUv.x * 8.0);
    vec3 color = mix(a, b, wave);
    gl_FragColor = vec4(color, 1.0);
}
```

What matters is not memorizing syntax. Explain the data flow:

- `uTime` comes from CPU-side code;
- `vUv` identifies a position across the surface;
- every fragment evaluates the formula;
- the result becomes color.

## First Experiments

Change one thing at a time:

1. replace `vUv.x` with `vUv.y`;
2. increase the frequency multiplier;
3. combine x/y into radial distance;
4. replace sine with `fract`;
5. drive color from mouse position.

This is shader literacy: learning by perturbing equations and seeing the result immediately.

## Mini-Project: Procedural Signal Card

Create one fullscreen or plane-based visual with:

- animated color field;
- procedural lines/shapes;
- distortion;
- scanline/halftone treatment;
- mouse or audio-ready parameters;
- no required image texture for the core effect.

Expose its parameters from TypeScript if using the web.

## Performance Habit

Track frame time, not just frames per second.

```text
60 FPS ≈ 16.7 ms per frame
120 FPS ≈ 8.3 ms per frame
```

A beautiful shader that destroys the frame budget is unfinished engineering.

## Mistakes To Avoid

- trying to learn GLSL, WGSL, and HLSL simultaneously;
- writing CPU loops to update every particle when the GPU should own simulation;
- giant branches inside shaders without understanding cost;
- copying random shader snippets without understanding coordinate space;
- ignoring resolution/aspect ratio;
- optimizing from intuition instead of measuring GPU/frame cost.

## Ready For The Full Track?

You are ready when you can:

- explain vertex/fragment stages;
- describe UV coordinates;
- modify a simple shader intentionally;
- send time or mouse data from CPU-side code;
- create an animated procedural effect;
- explain why GPU execution is appropriate for the effect.

Continue: [GPU + Shader Programming Track](../tracks/gpu-shaders.md)

Pair with [TypeScript 101](typescript.md) for browser visuals or [C++ / Unreal 101](cpp-unreal.md) for engine rendering.
