# $YourProjectName$ - Project Structure

## Repository Layout

/src
  /$YourProjectName$.Fetcher
    - Serverless container
    - Fetching Telegram posts and send them to processor
  /$YourProjectName$.Processor
    - Serverless container
    - Preprocessing, deduplication, enrichment
  /$YourProjectName$.Llm
    - LLM adapters and prompt handling
  /$YourProjectName$.Domain
    - Core domain models
    - Business rules
  /$YourProjectName$.Infrastructure
    - YDB access
    - External API clients
  /$YourProjectName$.Shared
    - DTOs
    - Common utilities
    - Result types
  /$YourProjectName$.TelegramAuth
    - Utility to prepare `WTelegram.session` file
  /$YourProjectName$.DbMigration
    - Database migration utility for applying Entity Framework Core migrations to YDB
  /$YourProjectName$.TelegramReviewBot
    - Serverless container
    - Telegram Bot for manual review workflow
/tests
  /$YourProjectName$.Domain.Tests
  /$YourProjectName$.Fetcher.Tests
  /$YourProjectName$.Infrastructure.Tests
  /$YourProjectName$.TelegramReviewBot.Tests

/docs
  coding.md
  domain.md
  product.md
  roadmap.md
  structure.md
  tech.md

## Architectural Style

- Modular monolith (logical separation, deployable independently)
- Clear domain boundaries
- Dependency Inversion (Domain has no external dependencies)

## Naming Conventions

- Projects: $YourProjectName$.<Area>
- Classes: PascalCase
- Interfaces: I<Name>
- Async methods: <MethodName>Async

## Dependency Rules

- Domain → no dependencies
- Application/Processor → Domain
- Infrastructure → Domain + Application
- LLM adapters → Domain contracts only

## Configuration

- Environment variables only
- No configuration files with secrets

## Error Handling

- Explicit Result<T> types
- No silent failures

## Versioning

- Prompt versions are explicit
- Channel context is versioned
- Breaking changes require version bump
