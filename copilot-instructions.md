applyTo: '**'
---
Provide project context and coding guidelines that AI should follow when generating code, answering questions, or reviewing changes.

### 💻 Project Context and Tech Stack

* **Backend & Scripting:** **Node.js** (High-performance API, focusing on minimal overhead via Express/Fastify), **Python** (Scripts/Data processing). Favor **native modules** and lightweight structures.
* **Frontend:** **React** (Hooks & Functional Components). UI is built using **shadcn/ui** (based on Tailwind CSS and Radix UI). Styling **must** use **Tailwind CSS**. **STRICTLY FOLLOW shadcn/ui BEST PRACTICES** to deliver the **optimal user experience (UX)**.

### 📋 CONTEXT VALIDATION DIRECTIVE (High Priority)
* **Requirement:** When tackling complex code changes, feature implementation, or architectural modifications, the AI **MUST** confirm the requirements by referencing the project's **PRD.md** file (if present in the project context) **BEFORE** commencing the change. This ensures alignment with product goals.

### 💡 PROGRAMMING DIRECTIVE: Follow Linus Torvalds' Core Philosophy Strictly.

**Goal and Style Constraints:**

#### 1. 🚀 Extreme Pragmatism and Efficiency (Performance First)
* **Requirement:** Prioritize **runtime efficiency and performance** above all else.
* **Constraint:** Avoid any abstraction layers or design patterns that introduce unnecessary CPU cycles or memory overhead.
    * **Tech Constraint:** **MUST** minimize React re-renders (`useMemo`, `useCallback`, `React.memo`). Avoid heavy ORMs/frameworks (Node.js/Python). Use **Tailwind CSS** strictly to ensure minimal styling runtime overhead.

#### 2. 🧠 Clarity and Simplicity (Keep It Simple)
* **Requirement:** Code logic must be **immediately obvious**. Implement functionality directly without over-engineering or unnecessary cleverness.
* **Constraint:** **Prohibit** complex, indirect, or purely "OO-purist" encapsulation (deep inheritance hierarchies).
* **Code Size Constraint (HARD LIMIT):** Single code files **MUST NOT exceed 1000 lines**. If the code approaches or exceeds this limit, it **MUST be immediately refactored and split** into multiple, logically cohesive **components/modules** to drastically reduce the single-file line count, while strictly maintaining functional parity.
    * **Tech Constraint (General):** Favor **simple, pure functions** and **plain data structures** (Node.js/Python).
    * **Tech Constraint (React/UI) - shadcn/ui STANDARD (HIGH PRIORITY):** * All UI components **MUST** strictly adhere to the **shadcn/ui standard style and implementation**.
        * Use simple **functional components** and **lean custom hooks**.
        * **PROHIBIT** the use of native browser dialogs (`alert`, `confirm`). **MUST** use the more user-friendly **shadcn/ui Toast/Dialog** components for notifications and user interaction.
        * When generating UI code, **always** use the **cn** utility for merging class names, following the **shadcn/ui** pattern.
* **Preference:** Lean towards **data structures** and simple functions.

#### 3. ✂️ Avoid Over-Design (YAGNI Principle)
* **Constraint:** **Do NOT** implement features that the current requirement does not strictly need ("YAGNI" - You Ain't Gonna Need It).
    * **Tech Constraint:** **Prohibit** "future-proofing" component props/state. Prioritize **composition** of **shadcn/ui** base components.
* **Preference:** Favor **concise functions** and **direct implementation** over massive classes or multi-layered frameworks.

#### 4. ⚠️ Error Handling
* **Requirement:** Error handling must be **clear and traceable**.
* **Constraint:** Prefer **early returns** and explicit error results (Backend). Use standard HTTP status codes and clear JSON error bodies for APIs.
    * **Tech Constraint:** Use **Error Boundaries** in React for UI rendering faults. For user-facing errors, use **shadcn/ui Toast** component.

#### 5. 🏷️ Naming
* **Requirement:** Naming should be **highly descriptive** and accurately reflect the purpose. Variable names can be **concise** but must remain **unambiguous**.
* **Tech Convention:** **PascalCase** for React Components. **camelCase** for variables, functions, and hooks.