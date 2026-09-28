<h1 align="center">Hello, I am a Graphics Programmer 👋</h1>

<p align="center">
  Modern C++ and GLSL, rendering in real time.<br/>
  Building a cross-platform game engine to understand how everything fits together.
</p>

<p align="center">
  <img src="https://skillicons.dev/icons?i=cpp,cmake,clion,visualstudio,git,github,linux,windows&perline=8" alt="tech icons" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/C%2B%2B-17%20%7C%2020%20%7C%2023-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenGL-Core%20Profile-5586A4?style=for-the-badge&logo=opengl&logoColor=white" />
  <img src="https://img.shields.io/badge/GLSL-Shaders-5586A4?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Learning-Vulkan-AC162C?style=for-the-badge&logo=vulkan&logoColor=white" />
</p>

<p align="center">
  <a href="#-featured-project-impaction">Project</a> ·
  <a href="#-stack-layers">Stack</a> ·
  <a href="#-rendering-pipeline">Pipeline</a> ·
  <a href="#-toolchain">Toolchain</a> ·
  <a href="#-workflow">Workflow</a> ·
  <a href="#-roadmap">Roadmap</a> ·
  <a href="#-contact">Contact</a>
</p>

---

## 👤 About

I'm a graphics programmer focused on **real-time rendering for games and engines**. My primary language is **C++ (17/20)**, and I'm comfortable taking a project from an empty directory to a buildable, cross-platform codebase, including build systems and dependency management.

| | |
|---|---|
| 🎯 **Focus** | Real-time rendering, game engine development |
| 💻 **Language** | C++ 17 / 20 |
| 🎨 **Graphics** | OpenGL + GLSL |
| 🖥️ **Platforms** | Linux (primary) and Windows |

---

## 🎮 Featured Project: Impaction

**[staticinl/Impaction](https://github.com/staticinl/Impaction)** is a **cross-platform game engine** written in C++ with **OpenGL** as the graphics API. I'm building it from scratch to learn engine architecture and graphics programming hands-on, so the repo doubles as a running record of that work.

<p>
  <a href="https://github.com/staticinl/Impaction"><img src="https://img.shields.io/badge/repo-Impaction-181717?style=flat-square&logo=github" /></a>
  <img src="https://img.shields.io/badge/lang-C%2B%2B-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/api-OpenGL-5586A4?style=flat-square&logo=opengl&logoColor=white" />
  <img src="https://img.shields.io/badge/build-CMake-064F8C?style=flat-square&logo=cmake&logoColor=white" />
  <img src="https://img.shields.io/badge/platforms-Linux%20%7C%20Windows-lightgrey?style=flat-square" />
  <img src="https://img.shields.io/badge/contributors-welcome-brightgreen?style=flat-square" />
</p>

> 👯 **Open to contributors.** If engine architecture, rendering, or graphics programming interests you, issues and PRs are welcome.

---

## 🧱 Stack Layers

```mermaid
flowchart TB
    APP["🧩 Application layer<br/>C++17 / 20"]
    LIB["📚 Support libraries<br/>GLFW · Dear ImGui · stb"]
    API["🎨 Graphics API<br/>OpenGL + GLSL"]
    OS["🖥️ Platform<br/>Linux · Windows"]
    APP --> LIB --> API --> OS

    classDef app fill:#00599C,stroke:#003b69,color:#fff
    classDef lib fill:#064F8C,stroke:#03325a,color:#fff
    classDef api fill:#5586A4,stroke:#2f5871,color:#fff
    classDef os fill:#444,stroke:#222,color:#fff
    class APP app
    class LIB lib
    class API api
    class OS os
```

---

## 🎞️ Rendering Pipeline

```mermaid
flowchart LR
    subgraph CPU["🧠 CPU · C++"]
        direction LR
        A["Vertex data<br/>VBO / VAO"] --> B["State setup<br/>uniforms · textures"] --> C["Draw call<br/>glDrawElements"]
    end
    subgraph GPU["⚡ GPU · OpenGL pipeline"]
        direction LR
        D["Vertex Shader<br/>GLSL"] --> E["Primitive<br/>Assembly"] --> F["Rasterization"] --> G["Fragment Shader<br/>GLSL"] --> H["Depth · Stencil<br/>Blend"] --> I[("Framebuffer")]
    end
    C --> D

    classDef shader fill:#5586A4,stroke:#2f5871,color:#fff
    class D,G shader
```

---

## 🛠️ Toolchain

### Build and dev flow

```mermaid
flowchart LR
    A["✏️ Edit<br/>CLion · Visual Studio"] --> B["🔧 Configure<br/>CMake · Premake"]
    DEP["📦 Dependencies<br/>vcpkg · FetchContent · submodules"] --> B
    B --> C["🏗️ Build<br/>CMake · MSBuild"]
    C --> D["🧹 Format and lint<br/>clang-format · clang-tidy"]
    D --> E["🐞 Debug<br/>gdb · lldb · VS debugger"]
    E --> A
```

### Cross-platform build matrix

```mermaid
flowchart LR
    SRC["📁 One C++ codebase"] --> GEN["⚙️ CMake · Premake"]
    DEP["📦 vcpkg · FetchContent · submodules"] --> GEN
    GEN --> L["🐧 Linux<br/>CLion · gdb · lldb"]
    GEN --> W["🪟 Windows<br/>Visual Studio · MSBuild · VS debugger"]
```

### Full reference

| Category | Tools |
|---|---|
| **Language** | C++ 17 / 20 |
| **Graphics API** | OpenGL |
| **Shaders** | GLSL |
| **Libraries** | GLFW, Dear ImGui, stb |
| **Build systems** | CMake, Premake, MSBuild |
| **Dependencies** | vcpkg, Git submodules, CMake FetchContent |
| **IDEs** | CLion, Visual Studio |
| **Debuggers** | gdb, lldb, Visual Studio debugger |
| **Code quality** | clang-format and  clang-tidy |
| **OS** | Linux and  Windows |

---

## 🔁 Workflow

I add features **incrementally**: get the smallest part on screen often break it on purpose and then and learn from the issue it causes.

---

## 🗺️ Skill Map

```mermaid
mindmap
  root((Graphics<br/>Programmer))
    Languages
      C++ 17/20
      GLSL
    Graphics
      OpenGL
      Real-time rendering
      Game engines
    Build
      CMake
      Premake
      MSBuild
    Dependencies
      vcpkg
      FetchContent
      Git submodules
    Quality
      clang-format
      clang-tidy
    Platforms
      Linux
      Windows
```

---

## 📈 Status Matrix

| Technology | Status |
|---|---|
| C++ 17 / 20 | ✅ Daily driver |
| OpenGL | ✅ In use (Impaction) |
| GLSL | ✅ In use |
| CMake · Premake · MSBuild | ✅ In use |
| vcpkg · FetchContent · submodules | ✅ In use |
| clang-format · clang-tidy | ✅ In use |
| Vulkan | 🌱 Learning next |
| ECS architecture | 🌱 Learning next |
| GPU-driven rendering / compute | 🌱 Learning next |

---

## 🚀 Roadmap

```mermaid
timeline
    title Focus areas
    Now : OpenGL and GLSL : Modern C++ : Impaction engine
    Next : Vulkan : ECS architecture : GPU-driven rendering and compute
```

---

## 📫 Contact

- 📷 Instagram: https://instagram.com/staticinl
- 🎮 Discord: username-> staticinl
- 📧 Email: swapmit.13@gmail.com

---

<p align="center"><i>Follow along or contribute: <a href="https://github.com/staticinl/Impaction">staticinl/Impaction</a></i></p>
