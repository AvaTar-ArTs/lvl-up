# C++ / Unreal 101

C++ is the realtime runtime layer in `lvl-up`. Unreal gives the language a concrete habitat: gameplay systems, simulation, performance-sensitive code, engine architecture, and the path toward console-class development.

## Why Learn C++ Through Unreal

C++ in isolation can feel like a museum of sharp objects. Unreal gives those concepts jobs.

You learn pointers because objects have lifetimes. You learn references because systems share access. You learn classes/components because gameplay architecture needs boundaries. You learn profiling because realtime code has a frame budget.

## Toolchain Mental Model

```text
source/header files
      ↓
compiler + Unreal Build Tool
      ↓
module / executable
      ↓
Unreal Editor / runtime
```

You need an Unreal C++ project and a supported compiler/toolchain for your platform.

## Core C++ Concepts

Learn first:

- values and types;
- functions;
- references and pointers;
- `const`;
- structs and classes;
- constructors/destructors;
- stack vs heap;
- RAII;
- containers;
- ownership/lifetime;
- headers vs implementation files.

Then map them into Unreal concepts:

- `UObject`;
- `AActor`;
- `UActorComponent`;
- `APawn` / `ACharacter`;
- `AController`;
- `AGameMode`;
- subsystems;
- reflection macros;
- Blueprints as composition/presentation rather than a replacement for architecture.

## First Standard C++ Program

Before Unreal, understand one reference:

```cpp
#include <iostream>
#include <string>

struct Job {
    std::string id;
    float progress;
};

void PrintJob(const Job& job) {
    std::cout << job.id << ": " << job.progress * 100.0f << "%\n";
}

int main() {
    Job job{"render-001", 0.72f};
    PrintJob(job);
}
```

`const Job&` means the function can read the existing object without copying or modifying it.

## First Unreal Build

Create one C++ Actor with an editor-exposed property.

Conceptually:

```cpp
UCLASS()
class YOURPROJECT_API ALvlUpActor : public AActor
{
    GENERATED_BODY()

public:
    UPROPERTY(EditAnywhere, BlueprintReadWrite)
    float Intensity = 1.0f;
};
```

Compile, place it in a level, and change `Intensity` in the editor.

That tiny loop teaches the relationship between C++, Unreal reflection, generated code, and editor composition.

## Mini-Project: Interactable Component

Build a reusable interaction system:

1. create an `UActorComponent` that owns interaction behavior;
2. attach it to at least two different Actors;
3. expose presentation settings to Blueprints;
4. keep core state transitions in C++;
5. log invalid states clearly.

The goal is composition, not a giant inheritance tree.

## Mistakes To Avoid

- raw `new`/`delete` as your default ownership strategy;
- copying large objects because references feel unfamiliar;
- putting everything in one Actor;
- treating Tick as the solution to every behavior;
- mixing Unreal-managed objects with standard smart pointers without understanding ownership;
- optimizing before profiling;
- putting frame-by-frame gameplay logic in Python.

## PS5 Context

C++ and Unreal are appropriate public foundations for console-class development. Actual PlayStation SDK access, platform APIs, certification, packaging, and hardware workflows require authorization through Sony's developer program.

## Ready For The Full Track?

You are ready when you can:

- explain values, references, pointers, and lifetime at a practical level;
- compile a tiny C++ program;
- create a C++ Unreal Actor;
- expose a property to the editor;
- understand Actor vs Component conceptually;
- explain what belongs in C++ versus Blueprint versus Python.

Continue: [C++ + Unreal Track](../tracks/cpp-unreal.md)

Study alongside: [GPU / Shaders 101](gpu-shaders.md).
