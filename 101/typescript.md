# TypeScript 101

TypeScript is JavaScript with a type system. In this stack it is the product/interface layer: browsers, dashboards, Node tools, MCP surfaces, APIs, and interactive control panels.

## Why Learn It Here

Python already owns much of the intelligence and automation. TypeScript gives those systems a visible, interactive front door.

```text
TypeScript UI / Node
        ↓
API / process boundary
        ↓
Python workflows
```

## Toolchain

Verify Node and a package manager:

```bash
node --version
npm --version
```

Create a minimal project:

```bash
mkdir ts-101 && cd ts-101
npm init -y
npm install -D typescript tsx @types/node
npx tsc --init
```

Enable strict type checking in `tsconfig.json`.

## Core Concepts

Learn:

- JavaScript runtime basics;
- `const` and `let`;
- arrays and objects;
- functions;
- `type` and `interface`;
- unions;
- narrowing;
- generics;
- modules;
- Promises and `async`/`await`;
- JSON parsing;
- errors;
- browser vs Node runtime differences.

## First Program

Create `index.ts`:

```ts
type JobStatus = "queued" | "running" | "complete" | "failed";

type Job = {
  id: string;
  status: JobStatus;
  progress: number;
};

function summarize(job: Job): string {
  return `${job.id}: ${job.status} (${Math.round(job.progress * 100)}%)`;
}

const job: Job = {
  id: "render-001",
  status: "running",
  progress: 0.72,
};

console.log(summarize(job));
```

Run:

```bash
npx tsx index.ts
```

Now deliberately assign an invalid status and read the compiler/editor error.

## The Important Mental Shift

Types are not decoration. Use them to make invalid states harder to represent.

Instead of:

```ts
type Job = {
  status: string;
  result?: string;
  error?: string;
};
```

prefer a discriminated union when the state matters:

```ts
type Job =
  | { status: "queued" }
  | { status: "running"; progress: number }
  | { status: "complete"; result: string }
  | { status: "failed"; error: string };
```

## Mini-Project: Typed Workflow Viewer

Build a Node/TypeScript CLI that:

1. reads workflow JSON files;
2. converts them into typed domain objects;
3. rejects malformed records;
4. prints a useful summary;
5. outputs a normalized index.

Stretch: generate a tiny HTML page showing the workflows.

## Mistakes To Avoid

- using `any` to silence every type problem;
- assuming TypeScript validates unknown JSON at runtime;
- mixing browser-only and Node-only APIs casually;
- giant interfaces that model unrelated concerns;
- learning React before understanding TypeScript data flow;
- hiding asynchronous failures.

## Ready For The Full Track?

You are ready when you can:

- create and run a strict TS project;
- model data with unions/interfaces;
- explain compile-time vs runtime validation;
- use `async`/`await`;
- read/write JSON;
- understand what runs in Node versus the browser;
- call a Python process or HTTP endpoint conceptually.

Continue: [TypeScript Track](../tracks/typescript.md)

Then build toward the **Creative Workflow Control Center**.
