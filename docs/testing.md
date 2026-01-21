# Testing Guidelines

## 🧪 Test Types

- Unit tests — default
- Integration tests — when external systems involved

## 🧱 Structure

- Arrange / Act / Assert
- One logical behavior per test

## 🏷️ Naming

Recommended:

- MethodName_State_ExpectedResult
- Given_When_Then

## 🧰 Tools

- Test framework: xUnit (default)
- Mocking: Moq / NSubstitute

## ⚠️ Rules

- No sleeping or timing-based tests
- No random data without fixed seeds
- Tests must be deterministic
