# AGENTS.md — AI Development Rules

## 🎯 Purpose

This repository is a .NET project template designed for:

- Human developers
- AI IDE assistants (Kiro, Roo Code, Kilo Code)

AI agents must follow the rules described in this file and in `/docs`.

---

## 🧱 Technology Stack (baseline)

- Platform: .NET (LTS or latest stable)
- Language: C#
- Build: dotnet CLI
- Testing: xUnit (default), NUnit or MSTest allowed
- Mocking: Moq / NSubstitute / FakeItEasy
- No framework assumptions (no MediatR, no DDD requirement)

---

## 🗂️ Project Structure Rules

AI agents MUST:

1. Inspect `/docs/structure.md` before creating files
2. Follow existing folder conventions
3. Never invent new top-level folders without strong reason

---

## ✍️ Coding Rules

AI agents MUST:

- Follow `/docs/coding.md`
- Prefer readability over cleverness
- Use async/await where applicable
- Avoid premature abstractions
- Add XML documentation for public APIs

AI agents MUST NOT:

- Introduce hard-coded secrets
- Add unused dependencies
- Break existing public contracts without explanation

---

## 🧪 Testing Rules

AI agents MUST:

- Add or update tests for all non-trivial logic
- Follow `/docs/testing.md`
- Prefer deterministic tests
- Name tests descriptively (Given_When_Then or similar)

---

## 📚 Documentation Rules

- Architectural or behavioral changes MUST update `/docs`
- New patterns should be documented in `/docs/patterns.md`

---

## 🔁 Common AI Tasks

When asked to:

- **Add a feature** → check `docs/structure.md`, then `docs/coding.md`
- **Refactor code** → preserve behavior, update tests if needed
- **Fix a bug** → add a regression test first

---

## 🛑 Guardrails

AI agents must not:

- Rewrite large parts of the codebase unless explicitly requested
- Change architectural direction implicitly
- Optimize without measurable reason

If uncertain — ask for clarification.
