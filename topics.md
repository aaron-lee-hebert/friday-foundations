# Friday Foundations — 52-Week Learning Roadmap

## Quarter 1 — C# Fundamentals You May Have Glossed Over (Weeks 1–13)

- [x] **Week 1 — Value types vs. reference types** — How the stack and heap actually work, why it matters for structs, classes, and passing arguments by value vs. reference.
- [ ] **Week 2 — Boxing and unboxing** — What it is, when it happens silently, and the hidden performance cost hiding in legacy code.
- [ ] **Week 3 — The `using` keyword — all of it** — `using` directives, `using` statements, `using` declarations (C# 8+), and `IDisposable` properly implemented.
- [ ] **Week 4 — Delegates, `Func`, and `Action`** — What delegates actually are under the hood, why `Func<T>` and `Action<T>` exist, and how they connect to LINQ and events.
- [ ] **Week 5 — Events and the observer pattern in C#** — How `event` wraps a delegate, the publisher/subscriber contract, and EventHandler conventions.
- [ ] **Week 6 — Generics — beyond `List<T>`** — Generic constraints (`where T : class`, `new()`, `IComparable`), generic methods, and why they matter for reusable design.
- [ ] **Week 7 — Interfaces vs. abstract classes** — The real distinction, when to choose which, and why "program to an interface" isn't just a slogan.
- [ ] **Week 8 — Access modifiers — all of them** — `internal`, `protected internal`, `private protected`, and why `internal` is underused in well-structured assemblies.
- [ ] **Week 9 — LINQ — how it actually works** — Deferred execution, `IEnumerable<T>` vs. `IQueryable<T>`, and why this distinction breaks things silently in NHibernate.
- [ ] **Week 10 — Async/await — the real model** — The state machine under the hood, `ConfigureAwait(false)`, `Task` vs. `ValueTask`, and common deadlock traps in ASP.NET.
- [ ] **Week 11 — Nullable reference types (C# 8+)** — The `?` annotation system, what the compiler enforces vs. what it doesn't, and why null is called a "billion-dollar mistake."
- [ ] **Week 12 — Records and immutability (C# 9–12)** — `record`, `record struct`, `init`-only setters, `with` expressions, and where immutability improves reasoning.
- [ ] **Week 13 — Collections deep dive** — `List<T>` vs. `IList<T>` vs. `IReadOnlyList<T>`, `Dictionary<K,V>`, `HashSet<T>`, `Queue<T>`, and when to reach for each.

---

## Quarter 2 — Principles, Patterns, and Architecture (Weeks 14–26)

- [ ] **Week 14 — Single Responsibility Principle** — What a "reason to change" actually means, and how to diagnose bloated service classes in your current codebase.
- [ ] **Week 15 — Open/Closed Principle** — Extending behavior through abstraction rather than modification; how strategy and inheritance relate.
- [ ] **Week 16 — Liskov Substitution Principle** — Why subtype contracts matter, and how violated LSP causes subtle bugs in inheritance hierarchies.
- [ ] **Week 17 — Interface Segregation Principle** — Fat interfaces and their cost; how to identify them and break them apart.
- [ ] **Week 18 — Dependency Inversion Principle + DI in ASP.NET Core** — The principle vs. the container; `AddScoped` vs. `AddSingleton` vs. `AddTransient` and their real implications.
- [ ] **Week 19 — The Repository Pattern** — What it's really for (decoupling domain logic from data access), and why "NHibernate is already a unit of work" is a nuanced argument.
- [ ] **Week 20 — Factory Method Pattern** — When constructors aren't enough; how factories decouple object creation from usage.
- [ ] **Week 21 — Strategy Pattern** — Swapping algorithms at runtime; how it relates to DI and replaces large if/switch chains.
- [ ] **Week 22 — Decorator Pattern** — Layering behavior without inheritance; why it's the pattern behind middleware and logging wrappers.
- [ ] **Week 23 — Template Method Pattern** — Defining a skeleton algorithm with overridable steps; when it's cleaner than strategy.
- [ ] **Week 24 — YAGNI, DRY, KISS, and when they conflict** — These principles frequently pull against each other; learning to negotiate them is senior-engineer territory.
- [ ] **Week 25 — Software architecture patterns — Layered vs. Clean** — The difference between N-tier layered architecture and Clean/Onion; dependency direction as the key distinction.
- [ ] **Week 26 — Domain-Driven Design — Core Vocabulary** — Entities, value objects, aggregates, bounded contexts — not as a full implementation but as a vocabulary for thinking about your domain.

---

## Quarter 3 — Data, Testing, and APIs (Weeks 27–39)

- [ ] **Week 27 — TDD — the red-green-refactor discipline** — The three rules of TDD (Uncle Bob's), why the test is a design tool, and what makes a failing test meaningful.
- [ ] **Week 28 — Unit testing styles — output, state, and communication-based** — Deepened with NUnit-specific examples across all three styles.
- [ ] **Week 29 — Mocking vs. stubbing vs. faking** — The vocabulary matters; NSubstitute's `Substitute.For<T>()`, `Returns()`, `Received()`, and when not to mock.
- [ ] **Week 30 — Writing testable code** — Seams, pure functions, avoiding `new` inside logic, and why static methods are a testing hazard.
- [ ] **Week 31 — Test data — Bogus and AutoFixture** — Generating realistic, randomized test data; property-based thinking.
- [ ] **Week 32 — Integration testing with `WebApplicationFactory`** — Testing the full ASP.NET Core pipeline in-process; when integration tests beat unit tests.
- [ ] **Week 33 — Dapper — the fundamentals** — `Query<T>`, `Execute`, `QueryMultiple`, parameter handling, and how it compares to raw ADO.NET.
- [ ] **Week 34 — Dapper — advanced patterns** — Multi-mapping (`splitOn`), dynamic parameters, stored procedure calls, and transaction handling.
- [ ] **Week 35 — NHibernate vs. Dapper — when to use which** — N+1, lazy loading costs, and where dropping to Dapper in an NHibernate codebase makes sense.
- [ ] **Week 36 — SQL query optimization basics** — Execution plans, index seeks vs. scans, covering indexes, and reading the queries NHibernate generates.
- [ ] **Week 37 — PostgreSQL vs. SQL Server — key differences** — Data types, string case sensitivity, sequence vs. identity, `ILIKE`, `RETURNING`, `JSONB`, and CTE behavior differences.
- [ ] **Week 38 — REST API design principles** — Resource naming, HTTP verb semantics, status code discipline, and what "RESTful" actually means vs. how it's commonly misused.
- [ ] **Week 39 — Middleware pipeline in ASP.NET Core** — What middleware is, the `Use`/`Run`/`Map` distinction, order matters, and building custom middleware.

---

## Quarter 4 — Modern .NET Ecosystem and the Outer Edges (Weeks 40–52)

- [ ] **Week 40 — Authentication and authorization in ASP.NET Core** — The difference between the two, `[Authorize]`, policy-based auth, and how JWT works end-to-end.
- [ ] **Week 41 — JWT and OAuth 2.0 — demystified** — What's in a token, how `Bearer` auth works, and when to reach for IdentityServer or Azure AD instead.
- [ ] **Week 42 — Caching strategies — memory cache vs. distributed cache** — `IMemoryCache`, `IDistributedCache`, cache invalidation as the "hard problem," and Redis as the answer.
- [ ] **Week 43 — Logging with Serilog** — Structured logging vs. string interpolation, sinks, enrichers, and why `{@Property}` beats `{Property.ToString()}`.
- [ ] **Week 44 — Background tasks — Hosted Services** — `IHostedService` vs. `BackgroundService`, the hosted service lifecycle, and where HangFire adds value over raw hosted services.
- [ ] **Week 45 — CQRS — Commands, Queries, and MediatR** — The pattern itself (separate read/write models), then how MediatR implements it with `IRequest<T>` and handlers.
- [ ] **Week 46 — Resilience with Polly** — Retry, circuit breaker, timeout, and bulkhead policies; how `Microsoft.Extensions.Http.Resilience` wraps Polly in .NET 8+.
- [ ] **Week 47 — FluentValidation** — Separating validation logic from models; rule chaining, custom validators, and integration with ASP.NET Core's model pipeline.
- [ ] **Week 48 — OpenTelemetry — traces, metrics, and logs** — The three pillars of observability, what a span is, and how to instrument an ASP.NET Core app.
- [ ] **Week 49 — Docker fundamentals for .NET developers** — Writing a `Dockerfile` for an ASP.NET Core app, multi-stage builds, and why containers solve the "works on my machine" problem.
- [ ] **Week 50 — CI/CD concepts applied to Azure DevOps** — Pipeline stages, artifacts, build vs. release pipelines, and the specific Azure DevOps patterns you're already working in.
- [ ] **Week 51 — Semantic Kernel and working with LLMs in .NET** — What Semantic Kernel is, its plugin model, and how to make a simple AI-powered call from a .NET app.
- [ ] **Week 52 — Reflection on the year — 10X in practice** — Not a new topic, but a structured retrospective: what compounded, what didn't, and what the roadmap looks like for year two.