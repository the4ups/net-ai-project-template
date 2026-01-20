# $YourProjectName$ - Roo AI IDE Guidelines

## 🔄 Project Awareness & Context

- **Always read the project's general documentation files** at the beginning of a new discussion to understand the project's architecture, goals, style, and constraints.
- **Follow `roadmap.md`** before starting task. If task not exists in active Phase, add it with short description and current date.
- **Follow the established naming conventions, folder structure, and architectural patterns** described in `structure.md`.

## 📚 General Project Documentation

### Tech Stack

See [docs/tech.md](../../docs/tech.md)

### Product Description

See [docs/product.md](../../docs/product.md)

### Project Structure

See [docs/structure.md](../../docs/structure.md)

### Coding Standards

See [docs/coding.md](../../docs/coding.md)

### Domain Rules

See [docs/domain.md](../../docs/domain.md)

### Project Roadmap

See [docs/roadmap.md](../../docs/roadmap.md)

---

## 🧱 Code Structure & Modularity

- **Do not create files longer than 500 lines of code.** When approaching the limit, refactor the code by splitting it into classes, namespaces, or helper files.
- **Organize code into clearly separated modules and namespaces**, grouped by functionality or responsibility.
- **Use clear and consistent `using` directives**, preferably only the necessary ones and at the beginning of the file.

---

## 🧪 Testing & Reliability

**Mandatory Testing Strategy for All Features:**

1. **Create comprehensive unit tests** (xUnit/NUnit) covering:
   - Expected behavior (happy path)
   - Boundary cases
   - Error scenarios
   - Integration points with mocks/stubs

2. **Complement with Property-Based Tests** (FsCheck/Hedgehog/etc.):
   - Define universal properties that must hold for all valid inputs
   - Generate random inputs across full parameter ranges
   - Include edge cases automatically
   - Run minimum 100 iterations per property

3. **Test Structure & Organization:**
   - Place tests in `/tests` folder mirroring main code structure
   - Tag property tests clearly: `"Feature: {feature_name}, Property {n}: {description}"`
   - Use smart generators for complex domain objects

4. **Maintenance Discipline:**
   - Update tests when logic changes
   - Ensure tests remain independent and reliable
   - Include integration/e2e tests for critical workflows

**Core Principle:** Tests should prove correctness, not just verify examples. Combine specific scenarios (unit tests) with universal verification (property tests).

---

## 📚 Documentation & Explainability

- Update README.md when adding new features, changing dependencies, or setup steps.
- Comment complex or non-obvious code so it can be understood by a mid-level developer.
- For complex logic, add inline comments with `// Reason:` — explain *why*, not just *what* the code does.

## 🧠 AI Behavior Rules

- Do not make assumptions about missing context — ask questions if unsure.
- Do not invent libraries or functions — use only proven and well-known .NET and NuGet packages.
- Always check the existence of file paths and the names of namespaces and classes before referencing them in code or tests.
- Do not delete or rewrite existing code unless there is an explicit instruction or task from TASK.md.

## 🔧 Roo-specific Rules

- Utilize Roo's capabilities for code analysis and refactoring.
- Follow Roo's standard practices for project navigation.
- Apply Roo-specific tools for code optimization.

## External Tools Integration

Always use the context7 MCP server when needed for:

code generation,

executing setup or configuration steps,

working with library and API documentation.

This means you automatically consult context7 tools to obtain library identifiers and documentation without additional prompts.
