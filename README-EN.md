# Cursor-Unity-Rules-Workflow

### 🎮 A State-Driven AI Development Workflow for Unity (Cursor Edition)

> **True Vibe Coding: Not just prompts, but an industrialized virtual team.**

## 💡 Credits & Inspiration

The core philosophy of this project (Evolution Nodes & Pipeline Thinking) is deeply inspired by **Bilibili Creator @AI-Ghost-Lab**'s Codex Pipeline concept.

I have adapted and refactored this specifically for **Unity Game Development** (considering Components, Lifecycle, and Heavy Assets), transforming it into an interactive configuration compatible with **Cursor / Windsurf**.

> **Special Thanks to:** 🎥 [**Codex Pipeline: How to make AI your true coding assistant**](https://www.bilibili.com/video/BV1ktUgB9Evp/) 👤 **@AI-Ghost-Lab**

## ⚠️ Philosophy: Interface First

**This is NOT a magic wand for spaghetti code.**

The underlying logic of this workflow is **"Contract-Based Programming"**. To maximize AI efficiency and prevent Context Overflow, your project MUST follow a **Decoupled Architecture**.

### Best Practices

1. **Human Defines Contracts:** You are responsible for writing `Interfaces` (e.g., `IDamageable`, `IInteractable`) or abstract base classes. You define the boundaries of the system.
2. **AI Implements Details:** Through **Evolution Nodes**, you lock the state, allowing AI to fill in the specific logic implementation.
3. **No Tight Coupling:** If your code is full of direct cross-script references, AI will struggle to understand the context. Prioritize using an **Event Bus** or **Dependency Injection (DI)**.

> **"Don't let AI guess your architecture. You define the structure; AI fills the void."**

## 🤖 Virtual Studio Architecture

This is not just a set of prompts; it is a **7-person elite team** residing in your IDE. Through dynamic routing in `.cursorrules`, AI automatically switches roles based on your intent.

| **Role**            | **Alias**        | **Core Responsibility**                                      | **Typical Trigger**                                          |
| ------------------- | ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **Project Manager** | `The Razor`      | **Scope Control**. Manages Vertical Slice scope, rejecting any features irrelevant to the core experience. | "I want to add an inventory system...""Daily progress check" |
| **Historian**       | `Time Keeper`    | **State Management**. Maintains the `_Evolution` directory, creates `manifest.md`, ensuring no context loss. | "Start a new task...""Recap previous changes"                |
| **Architect**       | `Blueprinter`    | **System Design**. Writes `ledger.json` (construction blueprint), plans technical solutions, **NO coding**. | "How to design the weapon system?""How to decouple this?"    |
| **Tech Designer**   | `Pipeline Guard` | **Data & Pipeline**. Defines `ScriptableObject` structures, writes Editor tools, bridges Design and Code. | "Config enemy data...""Write an inspector tool"              |
| **Coder**           | `Executor`       | **Coding**. Reads `ledger.json` to execute tasks. Strictly follows SOLID and P0 constraints. | "Start coding...""Fix this bug"                              |
| **QA**              | `Gatekeeper`     | **Review**. Checks for P0 violations (e.g., Singletons, Hardcoding), generates review reports. | "Review my code""Check for potential bugs"                   |
| **Mentor**          | `Translator`     | **Concept Translation**. Explains Unity concepts using Java/Spring analogies for backend developers. | "What is a ServiceLocator?""What is a Bean in Unity?"        |

## 🔄 Standard Operating Procedure (SOP)

A typical feature development loop looks like this:

1. **Planning**: User proposes an idea $\rightarrow$ **@Historian** creates an Evolution Node $\rightarrow$ **@PM** reviews scope (Pass/Kill).
2. **Design**: **@Architect** breaks down requirements $\rightarrow$ Generates `ledger.json` $\rightarrow$ **@TD** defines data structures.
3. **Execution**: **@Coder** reads the ledger $\rightarrow$ Writes `C#` code $\rightarrow$ Updates ledger status.
4. **Review**: **@QA** reviews code $\rightarrow$ Flags P0/P1 issues $\rightarrow$ **@Coder** fixes issues $\rightarrow$ Completion.

## 🚀 Quick Start

### 1. Installation

1. Download this repository (or use the Template function).
2. Copy the `.cursor/` folder and `.cursorrules` file to the **root** of your Unity project.
3. **Important:** Check the `Files & Paths` section in `.cursorrules` to ensure paths match your project structure.

### 2. Init Evolution

Type in Cursor Chat:

> "Hi, I want to start a new feature. @historian"

### 3. Start Vibe Coding

AI will guide you through the loop:

- **Manifest:** Record requirements.
- **Ledger:** Architect generates the JSON blueprint.
- **Coding:** Coder implements the logic.
- **Review:** QA validates compliance.

## 🛡️ P0 Constraints

This configuration includes built-in **Absolute Defense Mechanisms** for industrial-grade Unity development. Violations will be rejected by the Architect and QA:

- ❌ **No Singletons:** Strictly prohibited. Use `ServiceLocator`.
- ❌ **No Instantiate:** Strictly prohibited. Use `SpawnManager` / Object Pooling.
- ❌ **No Hardcoding:** Magic numbers are forbidden. Use Data-Driven `ScriptableObjects`.
- ❌ **No Spaghetti:** Enforce separation of **View** and **Logic**. Logic layers must never reference `Animator` or `UI` directly.
- ❌ **No Input.GetKey:** Direct input polling is forbidden. Use `InputSystem` service.

## 📂 Recommended Structure

To maximize the effectiveness of this workflow, the following Unity project structure is recommended:

```
Assets/
├── _Evolution/          <-- [CORE] History records (Auto-managed by AI)
│   ├── 001_Init/
│   │   ├── manifest.md  <-- Requirements
│   │   └── ledger.json  <-- Blueprint
├── _Project/            <-- Your Game Assets
│   ├── Core/            <-- Architecture (ServiceLocator, Events, Input)
│   ├── Systems/         <-- Business Logic (Weapon, Player, Enemy)
│   └── Configs/         <-- ScriptableObjects (Data)
```

## 🤝 Contributing

Feel free to submit PRs or Issues to share your custom `.mdc` roles or new architectural insights.

License: MIT