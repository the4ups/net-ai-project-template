# C# Coding Rules (LLM Prompt)

You generate **production-ready C# code**.

## General

* Use **modern C# (.NET 12+)**
* Follow **Microsoft C# coding conventions**
* Prefer **clarity and explicitness** over cleverness
* Avoid magic numbers and strings
* Favor **immutability**
* Output must compile

## Style

* Nullable reference types enabled
* Strong typing, no `dynamic`
* Use modern C# features when they improve readability
* Keep methods small and single-purpose
* Use `var` only when the type is obvious
* Format code as `dotnet format`

## Naming

* PascalCase: classes, records, public members
* camelCase: locals, parameters, private fields
* Interfaces start with `I`
* Async methods end with `Async`
* Avoid obscure abbreviations

## Architecture

* Follow **SOLID**
* Clear separation of concerns
* Prefer composition over inheritance
* No premature abstractions
* No static state without strong justification

## Dependency Injection

* Constructor injection only
* No `IServiceProvider` usage
* Correct service lifetimes
* No service locator pattern

## Async

* Use `async/await` for all I/O
* Never use `.Result` or `.Wait()`
* Async all the way
* Pass `CancellationToken` when applicable

## Errors

* Do not swallow exceptions
* Exceptions are not control flow
* Catch only to handle or add context
* Use domain-specific exceptions when appropriate

## Validation

* Validate all external input
* Use FluentValidation or DataAnnotations
* Validation is separate from business logic

## Logging

* Structured logging only
* No sensitive data in logs
* Log important state changes and errors
* For LLM calls: log before/after, duration, status

## Documentation

* XML docs for all public APIs
* Comments explain **why**, not **what**

## Testing

* Unit test business logic
* Prefer pure functions
* Tests must be deterministic and readable

## Security

* Treat all input as untrusted
* No hardcoded secrets
* Follow secure defaults

## LLM Rules

* Do not invent APIs or types
* Prefer existing project patterns
* Choose the simplest reasonable solution
* Explain only non-obvious decisions
