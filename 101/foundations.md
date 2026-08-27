# Foundations 101

These are the skills that transfer between every language in `lvl-up`. Learn them once, then reuse them everywhere.

## 1. Terminal Literacy

Be comfortable with:

```bash
pwd
ls -la
cd path/to/project
mkdir demo
cp source target
mv old new
rm file
which python
which node
which cargo
echo $PATH
```

Understand the difference between the current directory, your home directory, absolute paths, relative paths, executables, and environment variables.

### Mini mission

Create a folder, add three text files, rename one, move one into a subfolder, and list the final tree from the terminal.

## 2. Git Literacy

The minimum loop:

```bash
git status
git add .
git commit -m "describe the change"
git log --oneline --decorate -10
git diff
git switch -c experiment
```

Know what a repository, commit, branch, remote, merge, conflict, tag, and pull request are.

### Rule

Git is not backup magic. A commit is a named checkpoint in the evolution of a project.

## 3. Build And Package Systems

Different ecosystems hide the same basic ideas behind different tools.

| Ecosystem | Common tool |
|---|---|
| Python | `pip`, `uv`, `venv`, `pyproject.toml` |
| TypeScript | `npm` / `pnpm`, `package.json`, `tsconfig.json` |
| Rust | Cargo, `Cargo.toml` |
| C++ | compiler + build system, often CMake or engine tooling |
| Swift | Swift Package Manager / Xcode |

Understand:

```text
source code → dependencies → compile/interpret → artifact → run
```

## 4. Processes And Boundaries

A program is a process. Processes can communicate through:

- command-line arguments;
- stdin/stdout;
- files;
- JSON/JSONL;
- HTTP;
- sockets;
- message queues;
- native function interfaces.

This becomes crucial once Python, TypeScript, Rust, C++, shaders, and Swift cooperate.

## 5. Data Literacy

Be comfortable reading and producing:

```json
{
  "id": "render-001",
  "status": "running",
  "progress": 0.72
}
```

Know arrays, objects/maps, strings, numbers, booleans, null/optional values, IDs, schemas, timestamps, and serialization.

## 6. HTTP And APIs

The mental model:

```text
client → request → server → response
```

Know the practical meaning of:

- URL
- method: GET/POST/PUT/PATCH/DELETE
- headers
- request body
- JSON response
- status code
- authentication token

You do not need to memorize HTTP. You need to understand the boundary.

## 7. Testing

Three useful layers:

```text
unit test        one small behavior
integration test multiple pieces together
end-to-end test  the real user/system flow
```

A test should answer a question, not merely increase a coverage number.

## 8. Debugging

When something fails:

1. reproduce it;
2. read the entire error;
3. find the first meaningful failure, not the last cascade;
4. shrink the problem;
5. inspect inputs and state;
6. form one hypothesis;
7. test it;
8. verify the fix against the original failure.

## 9. Performance

Never optimize from vibes.

```text
measure → identify bottleneck → change → measure again
```

Useful dimensions include:

- runtime;
- throughput;
- latency;
- memory;
- CPU;
- GPU frame time;
- startup time;
- file/network IO.

## 10. Documentation Literacy

Learn to look for:

- getting started;
- API reference;
- examples;
- migration/version notes;
- error documentation;
- package/library source when docs are insufficient.

## Foundations Mini-Project

Build a tiny cross-process job runner:

1. create a JSON job file;
2. write a Python script that reads it;
3. print structured JSON output;
4. invoke the script from the terminal;
5. commit it with Git;
6. intentionally break the JSON and diagnose the failure.

## Ready For The Language 101s?

You are ready if you can explain:

- where your program is running;
- how dependencies arrive;
- how input becomes output;
- how two processes could exchange data;
- how you would capture a checkpoint in Git;
- how you would begin debugging a failure.

Next: [Python 101](python.md) or jump directly to [TypeScript 101](typescript.md) if Python is already comfortable.
