# Technology Stack

## Language & Runtime

- C# (.NET 8+ LTS or latest stable)
- ASP.NET Core (if web application needed)

## Build & Testing

- dotnet CLI
- xUnit (default testing framework)
- Moq / NSubstitute (mocking)

## Data & Storage

- Entity Framework Core (if database needed)
- JSON for serialization

## Logging & Monitoring

- Microsoft.Extensions.Logging
- Structured logging

## Configuration

- Microsoft.Extensions.Configuration
- Environment variables for secrets

## Deployment

- Docker (optional)
- Cloud-agnostic by default

## Constraints

- No framework lock-in (MediatR, etc.)
- Prefer standard .NET libraries
- Keep dependencies minimal
