---
agent: "agent"
model: Claude Sonnet 4.5
description: "Ensure .NET/C# code meets best practices for the solution/project."
---

# .NET/C# Best Practices

Your task is to ensure .NET/C# code in ${selection} meets the best practices specific to this solution/project. This includes:

## Documentation & Structure
- **XML Documentation**: Create comprehensive XML documentation comments for all public classes, interfaces, methods, and properties.
- **Details**: Include parameter descriptions and return value descriptions in XML comments.
- **Namespaces**: Follow the established namespace structure: `{Core|Console|App|Service}.{Feature}`.

## Design Patterns & Architecture
- **Primary Constructors**: Use primary constructor syntax for dependency injection (e.g., `public class MyClass(IDependency dependency)`).
- **Command Handler**: Implement the Command Handler pattern with generic base classes (e.g., `CommandHandler<TOptions>`).
- **Interfaces**: Use interface segregation with clear naming conventions (prefix interfaces with 'I').
- **Factory Pattern**: Follow the Factory pattern for complex object creation.

## Dependency Injection & Services
- **Constructor Injection**: Use constructor dependency injection with null checks via `ArgumentNullException`.
- **Lifetimes**: Register services with appropriate lifetimes (Singleton, Scoped, Transient).
- **Patterns**: Use `Microsoft.Extensions.DependencyInjection` patterns.
- **Testability**: Implement service interfaces for testability.

## Resource Management & Localization
- **ResourceManager**: Use `ResourceManager` for localized messages and error strings.
- **Separation**: Separate `LogMessages` and `ErrorMessages` resource files.
- **Access**: Access resources via `_resourceManager.GetString("MessageKey")`.

## Async/Await Patterns
- **Async All the Way**: Use async/await for all I/O operations and long-running tasks.
- **Return Types**: Return `Task` or `Task<T>` from async methods.
- **ConfigureAwait**: Use `ConfigureAwait(false)` where appropriate (library code).
- **Exceptions**: Handle async exceptions properly.

## Testing Standards
- **Framework**: Use MSTest framework with FluentAssertions for assertions.
- **Pattern**: Follow AAA pattern (Arrange, Act, Assert).
- **Mocking**: Use Moq for mocking dependencies.
- **Coverage**: Test both success and failure scenarios.
- **Validation**: Include null parameter validation tests.

## Configuration & Settings

- Use strongly-typed configuration classes with data annotations
- Implement validation attributes (Required, NotEmptyOrWhitespace)
- Use IConfiguration binding for settings
- Support appsettings.json configuration files

## Semantic Kernel & AI Integration

- Use Microsoft.SemanticKernel for AI operations
- Implement proper kernel configuration and service registration
- Handle AI model settings (ChatCompletion, Embedding, etc.)
- Use structured output patterns for reliable AI responses

## Error Handling & Logging

- Use structured logging with Microsoft.Extensions.Logging
- Include scoped logging with meaningful context
- Throw specific exceptions with descriptive messages
- Use try-catch blocks for expected failure scenarios

## Performance & Security

- Use C# 12+ features and .NET 8 optimizations where applicable
- Implement proper input validation and sanitization
- Use parameterized queries for database operations
- Follow secure coding practices for AI/ML operations

## Code Quality

- Ensure SOLID principles compliance
- Avoid code duplication through base classes and utilities
- Use meaningful names that reflect domain concepts
- Keep methods focused and cohesive
- Implement proper disposal patterns for resources
