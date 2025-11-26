---
agent: "agent"
model: Claude Sonnet 4.5
tools: ["runCommands"]
description: "Get best practices for Entity Framework Core"
---

# Entity Framework Core Best Practices

Your goal is to help me follow best practices when working with Entity Framework Core.

## Data Context Design
- **Cohesion**: Keep `DbContext` classes focused and cohesive.
- **Injection**: Use constructor injection for configuration options.
- **Configuration**: Override `OnModelCreating` for fluent API configuration.
- **Separation**: Separate entity configurations using `IEntityTypeConfiguration`.
- **Factory**: Consider using `DbContextFactory` pattern for console apps or tests.

## Entity Design
- **Keys**: Use meaningful primary keys (consider natural vs surrogate keys).
- **Relationships**: Implement proper relationships (one-to-one, one-to-many, many-to-many).
- **Validation**: Use data annotations or fluent API for constraints and validations.
- **Navigation**: Implement appropriate navigational properties.
- **Value Objects**: Consider using owned entity types for value objects.

## Performance
- **NoTracking**: Use `AsNoTracking()` for read-only queries.
- **Pagination**: Implement pagination for large result sets with `Skip()` and `Take()`.
- **Eager Loading**: Use `Include()` to eager load related entities when needed.
- **Projection**: Consider projection (`Select`) to retrieve only required fields.
- **Compiled Queries**: Use compiled queries for frequently executed queries.
- **N+1**: Avoid N+1 query problems by properly including related data.

## Migrations
- **Scope**: Create small, focused migrations.
- **Naming**: Name migrations descriptively.
- **Verification**: Verify migration SQL scripts before applying to production.
- **Bundles**: Consider using migration bundles for deployment.
- **Seeding**: Add data seeding through migrations when appropriate.

## Querying
- **Execution**: Use `IQueryable` judiciously and understand when queries execute.
- **LINQ**: Prefer strongly-typed LINQ queries over raw SQL.
- **Operators**: Use appropriate query operators (`Where`, `OrderBy`, `GroupBy`).
- **Functions**: Consider database functions for complex operations.
- Implement specifications pattern for reusable queries

## Change Tracking & Saving

- Use appropriate change tracking strategies
- Batch your SaveChanges() calls
- Implement concurrency control for multi-user scenarios
- Consider using transactions for multiple operations
- Use appropriate DbContext lifetimes (scoped for web apps)

## Security

- Avoid SQL injection by using parameterized queries
- Implement appropriate data access permissions
- Be careful with raw SQL queries
- Consider data encryption for sensitive information
- Use migrations to manage database user permissions

## Testing

- Use in-memory database provider for unit tests
- Create separate testing contexts with SQLite for integration tests
- Mock DbContext and DbSet for pure unit tests
- Test migrations in isolated environments
- Consider snapshot testing for model changes

When reviewing my EF Core code, identify issues and suggest improvements that follow these best practices.
