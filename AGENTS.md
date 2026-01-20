# AGENTS.md

You are an AI agent working inside this repository.
These rules define the **contract** between you and the project.

Follow them strictly.

---

## MUST — Hard Rules

### 1. Project Context

* Always read and respect:

  * `docs/structure.md`
  * `docs/tech.md`
  * `docs/coding.md`
  * `docs/domain.md` (if present)
  * `docs/product.md` and `docs/roadmap.md` (if relevant)
* If requirements, domain rules, or architecture are unclear, **ask questions before writing code**.
* Do not guess missing requirements.

### 2. Code Quality

* Generate **production-ready, compilable C# code**.
* Follow all conventions defined in `docs/coding.md`.
* Respect existing project patterns and naming.
* Do not invent APIs, libraries, infrastructure, or abstractions.
* Do not introduce breaking changes without explicit confirmation.

### 3. Architecture

* Enforce strict layer boundaries:

  * **Domain → Application → Infrastructure**
* Domain layer must not depend on Application or Infrastructure.
* Prefer composition over inheritance.
* Avoid static state unless explicitly justified.
* Do not introduce abstractions prematurely.

### 4. Testing

* Every new or changed behavior **must include tests**.
* Tests must cover:

  * happy path
  * boundary cases
  * error cases
* Tests must be deterministic, readable, and isolated.
* Use property-based tests **only when domain logic benefits from invariants and broad input coverage**.

### 5. Security

* Treat all external input as untrusted.
* Never hardcode secrets, tokens, or credentials.
* Do not log sensitive or personal data.
* Follow secure defaults and OWASP best practices.

---

## SHOULD — Strong Recommendations

* Prefer simple and explicit solutions.
* Keep files small and focused (avoid files larger than ~500 lines).
* Prefer pure functions where possible.
* Add or update documentation in `docs/*.md` when implementing non-trivial features.
* Explain **non-obvious decisions** briefly in code or comments.
* Maintain consistency with existing code over introducing new patterns.

---

## CONTEXT — Guidance

* This project values **clarity over cleverness**.
* Consistency and maintainability are more important than micro-optimizations.
* If multiple valid solutions exist, choose the simplest reasonable one.
* When in doubt, ask before acting.

---

## Tooling & Workflow

* Use standard .NET CLI commands when needed:

  * `dotnet build`
  * `dotnet test`
  * `dotnet format`
* Do not assume CI/CD behavior unless documented.
* Generated code should pass existing tests without modification unless explicitly requested.

---

`AGENTS.md` is the **single source of truth** for AI agent behavior in this project.
