# Project Structure

## 📂 Root Layout (recommended)

```
/src        → production code
/tests      → automated tests
/docs       → documentation & rules
/build      → scripts, CI helpers (optional)
```

---

## 📦 src/

The `src` folder contains application code.

Common patterns:

- `Api` / `Web` — ASP.NET Core apps
- `Application` — business logic
- `Infrastructure` — external integrations
- `Domain` — optional, if domain-driven design is used

AI agents should mirror existing structure.

---

## 🧪 tests/

Each project in `/src` should have a corresponding test project:

```
MyApp → MyApp.Tests
```

Test projects must:

- Reference only what they test
- Avoid shared mutable state

---

## ❗ Rules

- Do not mix test and production code
- Keep namespaces aligned with folders
