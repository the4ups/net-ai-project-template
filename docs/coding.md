# Coding Guidelines

## ✨ General

- Prefer simple, explicit code
- Avoid magic numbers and strings
- One responsibility per class

## 🧵 Async & Concurrency

- Use async/await for I/O
- Avoid .Result and .Wait()

## 🧱 Classes & Methods

- Small classes, short methods
- Public APIs must be documented
- Use records for immutable data when appropriate

## 📛 Naming

- PascalCase: types, methods, properties
- camelCase: local variables
- Interfaces prefixed with I

## 🪵 Logging

- Use ILogger<T>
- No logging in domain-only logic unless required

## ❌ Avoid

- God classes
- Hidden side effects
- Static mutable state
