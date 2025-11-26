---
description: 'Guidelines for building REST APIs with ASP.NET'
applyTo: '**/*.cs, **/*.json'
---

# ASP.NET REST API Development Standards

## Context
These instructions apply when generating or modifying ASP.NET Core Web API projects.

## API Design Principles
- **Architecture**: Follow REST architectural principles. Use resource-oriented URLs and appropriate HTTP verbs (GET, POST, PUT, DELETE).
- **Minimal APIs vs Controllers**:
    - Use **Minimal APIs** for microservices, simple endpoints, and performance-critical scenarios.
    - Use **Controllers** for complex application logic, when extensive filter usage is required, or for larger, structured APIs.
- **Status Codes**: Return precise HTTP status codes (e.g., 201 Created, 204 No Content, 400 Bad Request, 404 Not Found).
- **Content Negotiation**: Support JSON as the default content type.

## Project Structure
- **Organization**: Organize code by feature (Feature Folders) or by domain (DDD) rather than technical layers (Controllers, Models) for larger projects.
- **Separation of Concerns**: Maintain clear separation between API layer, Business Logic/Services, and Data Access.
- **Configuration**: Use `appsettings.json` and Environment Variables for configuration. Use the Options pattern for strongly-typed configuration.

## Implementation Standards
- **Dependency Injection**: Use Constructor Injection for all dependencies. Avoid Service Locator pattern.
- **Validation**: Use FluentValidation or Data Annotations for model validation.
- **Async/Await**: Always use async/await for I/O operations. Avoid `.Result` or `.Wait()`.
- **ActionResult**: Use `ActionResult<T>` for clear return type documentation in Swagger.

## Data Access (Entity Framework Core)
- **Context**: Use `DbContext` with constructor injection.
- **Queries**: Use `AsNoTracking()` for read-only queries.
- **Migrations**: Use Code-First migrations.
- Demonstrate repository pattern implementation and when it's beneficial.
- Show how to implement database migrations and data seeding.
- Explain efficient query patterns to avoid common performance issues.

## Authentication and Authorization

- Guide users through implementing authentication using JWT Bearer tokens.
- Explain OAuth 2.0 and OpenID Connect concepts as they relate to ASP.NET Core.
- Show how to implement role-based and policy-based authorization.
- Demonstrate integration with Microsoft Entra ID (formerly Azure AD).
- Explain how to secure both controller-based and Minimal APIs consistently.

## Validation and Error Handling

- Guide the implementation of model validation using data annotations and FluentValidation.
- Explain the validation pipeline and how to customize validation responses.
- Demonstrate a global exception handling strategy using middleware.
- Show how to create consistent error responses across the API.
- Explain problem details (RFC 7807) implementation for standardized error responses.

## API Versioning and Documentation

- Guide users through implementing and explaining API versioning strategies.
- Demonstrate Swagger/OpenAPI implementation with proper documentation.
- Show how to document endpoints, parameters, responses, and authentication.
- Explain versioning in both controller-based and Minimal APIs.
- Guide users on creating meaningful API documentation that helps consumers.

## Logging and Monitoring

- Guide the implementation of structured logging using Serilog or other providers.
- Explain the logging levels and when to use each.
- Demonstrate integration with Application Insights for telemetry collection.
- Show how to implement custom telemetry and correlation IDs for request tracking.
- Explain how to monitor API performance, errors, and usage patterns.

## Testing REST APIs

- Guide users through creating unit tests for controllers, Minimal API endpoints, and services.
- Explain integration testing approaches for API endpoints.
- Demonstrate how to mock dependencies for effective testing.
- Show how to test authentication and authorization logic.
- Explain test-driven development principles as applied to API development.

## Performance Optimization

- Guide users on implementing caching strategies (in-memory, distributed, response caching).
- Explain asynchronous programming patterns and why they matter for API performance.
- Demonstrate pagination, filtering, and sorting for large data sets.
- Show how to implement compression and other performance optimizations.
- Explain how to measure and benchmark API performance.

## Deployment and DevOps

- Guide users through containerizing their API using .NET's built-in container support (`dotnet publish --os linux --arch x64 -p:PublishProfile=DefaultContainer`).
- Explain the differences between manual Dockerfile creation and .NET's container publishing features.
- Explain CI/CD pipelines for ASP.NET Core applications.
- Demonstrate deployment to Azure App Service, Azure Container Apps, or other hosting options.
- Show how to implement health checks and readiness probes.
- Explain environment-specific configurations for different deployment stages.
