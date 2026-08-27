# Python 101

Python is the orchestration brain of this stack: automation, AI, research, data transformation, media pipelines, scripting, and glue.

This 101 is less about “learning Python from zero” and more about identifying the small set of fundamentals that make everything else easier.

## What Python Is Good At

Use Python when you want to:

- automate repetitive work;
- connect tools and APIs;
- prototype quickly;
- process data and files;
- orchestrate AI/agent workflows;
- script creative applications;
- build services where iteration speed matters more than extreme native performance.

## Toolchain

Verify:

```bash
python3 --version
python3 -m venv .venv
source .venv/bin/activate
python -m pip --version
```

A project should normally have an isolated environment and a clear dependency manifest.

## Core Concepts

Learn these first:

- variables and basic types;
- lists, dictionaries, tuples, sets;
- `if`, `for`, `while`;
- functions;
- imports and modules;
- exceptions;
- files and paths;
- JSON;
- classes/dataclasses when they clarify domain models;
- virtual environments;
- async only when the problem actually needs it.

## First Program

Create `job_summary.py`:

```python
import json
from pathlib import Path

path = Path("job.json")
job = json.loads(path.read_text())

print(f"{job['id']}: {job['status']}")
```

Create `job.json`:

```json
{
  "id": "render-001",
  "status": "queued"
}
```

Run:

```bash
python job_summary.py
```

Then change the JSON and confirm the program changes without editing the code.

## Upgrade It

Turn the script into a function:

```python
def summarize(job: dict) -> str:
    return f"{job['id']}: {job['status']}"
```

Then add a failure case for missing fields.

## Mini-Project: Workflow Manifest Inspector

Build a small CLI that:

1. accepts a path;
2. reads every `.json` file in that folder;
3. validates required fields;
4. prints a summary table;
5. exits non-zero when malformed files are found;
6. exports one combined `index.json`.

This project exercises files, data, functions, errors, CLI input, and structured output.

## Mistakes To Avoid

- one giant script with no functions;
- catching every exception and hiding the real error;
- global mutable state everywhere;
- installing dependencies globally;
- turning every problem into a class hierarchy;
- using async or multiprocessing before measuring a need;
- rewriting working Python in another language merely because that language is newer.

## Ready For The Full Track?

You are ready when you can:

- create and activate an environment;
- run a module/script predictably;
- read/write JSON and files;
- model a small domain with functions and data structures;
- surface useful errors;
- call another process or HTTP service;
- explain why a component should remain in Python.

Continue: [Python Leverage](../tracks/python-leverage.md)

Then: [TypeScript 101](typescript.md) to give Python systems interactive product surfaces.
