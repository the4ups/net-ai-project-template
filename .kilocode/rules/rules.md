# Project AI Rules — Roo / Kilo

## 📘 Project Context
- Always read the following *before* generating any code:
  - docs/structure.md
  - docs/tech.md
  - docs/coding.md
  - docs/domain.md
  - docs/product.md
  - docs/roadmap.md
- If a roadmap task does not exist for the request, ask for clarification.
- Respect established naming conventions, folder structure, and architectural patterns.

---

## 📁 Code Structure & Organization
- Do **not** create files longer than 500 lines.
- Organize code in clearly separated modules/namespaces by responsibility.
- Use minimal and necessary `using` directives at the top only.
- Follow domain-driven structure where business logic is separate from infrastructure.

---

## 🧪 Testing Requirements
**All new features must include tests:**
1. Unit tests covering:
   - Happy path
   - Boundary conditions
   - Error/exception cases
2. Property-based tests (≥100 iterations) where applicable.
3. Place tests inside `/tests` mirroring the implementation folder layout.
4. Tests must assert *correctness*, not just a passing example.

---

## 📚 Documentation & Clarity
- Update `README.md` on:
  - new features
  - setup changes
  - new dependencies
- Comment complex logic with:
  ```csharp
  // Reason: explain *why* this code exists, not what it does
  ```

* Use XML docs for all public APIs.

---

## 🤖 AI Behavior Rules (Generic)

* Ask questions if context is missing or ambiguous.
* **Do not invent libraries, functions, types, or APIs.**
* Use only well-known .NET or official NuGet packages.
* Always verify file paths, namespace names, and class names before referencing.
* Do not delete or rewrite existing code without an explicit task instruction.

---

## 📍 Kilo-Specific Rules

* Use Kilo analysis/refactor tools to:

  * identify unused code
  * suggest safe refactors
  * propose simplifications
* Respect Kilo code navigation and search commands for large changes.

---

## 🔌 External Tool Integration

* When needed, consult context7 MCP server for:

  * official library docs
  * API identifiers
  * schema and doc lookups

---

## ⚠️ Do Not

* Break existing public APIs unless specified
* Circumvent architectural layer boundaries
* Assume behaviour not explicitly documented
