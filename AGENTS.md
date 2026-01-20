# AGENTS.md

You are an AI agent working inside this repository.
You must follow these rules strictly.

---

## MUST (Hard Rules)

### Project Understanding

* Always read and respect:

  * `docs/structure.md`
  * `docs/tech.md`
  * `docs/coding.md`
  * `docs/domain.md` (if present)
* If requirements or context are missing or unclear, **ask questions before coding**.
* Do not guess domain rules or architecture.

### Code Quality

* Generate **production-ready, compilable C# code**.
* Follow rules defined in `docs/coding.md`.
* Respect architectural boundaries defined in `docs/structure.md`.
* Do not invent APIs, libraries, types, or infrastructure.
* Do not introduce breaking changes without explicit confirmation.

### Architecture

* Enforce clear layer boundaries:

  * Domain → Application → Infrastructure
* Domain layer must not depend on Application or Infrastructure.
* Prefer composition over inheritance.
* No static state without strong justification.

### Testing

* Every new behaviour must include tests.
* Tests must cover:

  * happy path
  * boundary cases
  * error cases
* Tests must be deterministic and readable.

### Security

* Treat all external input as untrusted.
* Never hardcode secrets, tokens, or credentials.
* Do not log sensitive data.

---

## SHOULD (Strong Recommendations)

* Prefer simple, explicit solutions.
* Keep files small and focused (avoid >500 lines).
* Prefer pure functions where possible.
* Add documentation to `docs/*.md` when implementing non-trivial features.
* Explain non-obvious decisions briefly.

---

## CONTEXT (Guidance)

* This project favors clarity over cleverness.
* Consistency with existing code is more important than introducing new patterns.
* If multiple valid approaches exist, choose the simplest one.
