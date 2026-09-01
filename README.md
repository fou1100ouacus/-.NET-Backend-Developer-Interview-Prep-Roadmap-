
# .NET Backend Interview Prep — 45-Day Schedule (5 hrs/day) — v2

---

## Week 1: C# Core (Days 1–5)

**Day 1**
- Core: ★ Value vs reference types, boxing/unboxing, nullable types, var vs explicit typing; 🆕 Boolean types & operators; 🆕 Arrays
- Extra: Pattern matching (switch expressions, `is`/`as`), tuples & deconstruction, nullable reference types / working with NULL (C# 8+)

**Day 2**
- Core: ★ IEnumerable vs IQueryable vs ICollection vs IList; Collections (List, Dictionary, HashSet, Queue/Stack); 🆕 Lists and Dictionaries deep dive
- Extra: Structs vs classes vs records; `Span<T>`/`Memory<T>` basics; immutable collections; 🆕 Strings deep dive & string interning; 🆕 StringBuilder deep dive (vs concatenation)

**Day 3**
- Core: ★ Delegates vs events vs Func/Action/Predicate (🆕 generic delegate types); ★ exception handling (try/catch/finally, custom exceptions, filters)
- Extra: Multicast delegates, custom `add`/`remove` event accessors, exception filter `when` clause; 🆕 Expressions & Casting/Type Conversion (boxing, `Convert`, `Parse`)

**Day 4**
- Core: Generics & constraints; ★ OOP four pillars with code examples; 🆕 OOP building blocks — Field & Constant, Methods (by value vs by reference), Constructor, Properties
- Extra: Extension methods, partial classes, static classes vs static members; 🆕 Operator Overloading

**Day 5**
- Core: Overloading vs overriding, access modifiers, OOP traps (diamond problem); ★ interface vs abstract class; 🆕 Enums
- Extra: Records `with`-expressions, init-only setters; 🆕 Debugging in C# (breakpoints, watch/immediate windows, conditional breakpoints); 🆕 Tuple type (Tuple vs ValueTuple)
- **Hands-on:** console order system using interfaces, generics, custom exceptions, then refactor with inheritance/polymorphism (e.g., `PaymentMethod` types)

## Week 2: SQL (Days 6–10)

**Day 6**
- Core: ★ Joins (inner, left, right, full, self-join)
- Extra: CTEs (`WITH` clause), subqueries vs joins, UNION vs UNION ALL

**Day 7**
- Core: ★ Clustered vs non-clustered indexes; normalization (1NF–3NF)
- Extra: Covering indexes, index seek vs scan, composite indexes

**Day 8**
- Core: ★ ACID properties + isolation levels
- Extra: Deadlocks and how to avoid them, optimistic vs pessimistic locking

**Day 9**
- Core: ★ GROUP BY/HAVING vs WHERE, window functions; stored procs/views/triggers
- Extra: PIVOT/UNPIVOT, ranking functions (ROW_NUMBER, RANK, DENSE_RANK)

**Day 10**
- Core: Query optimization (execution plans, avoiding SELECT *)
- Extra: Reading execution plans in practice, parameter sniffing
- **Hands-on:** design orders/customers/products schema, write 5–6 queries covering joins, aggregates, a window function, plus 1 CTE and 1 ranking-function query

## Week 3: EF Core (Days 11–15)

**Day 11**
- Core: DbContext/DbSet, Code First vs Database First, migrations
- Extra: Fluent API vs Data Annotations, data seeding

**Day 12**
- Core: ★ Tracking vs no-tracking; eager/lazy/explicit loading; relationships
- Extra: Global query filters, table splitting, inheritance mapping (TPH/TPT/TPC)

**Day 13**
- Core: ★ N+1 query problem, compiled queries, AsSplitQuery
- Extra: Interceptors, bulk operations (EFCore.BulkExtensions overview)

**Day 14**
- Core: Optimistic concurrency, explicit transactions, shadow properties, raw SQL; Repository/UoW debate
- Extra: Change tracking internals (snapshot vs proxy), DbContext pooling

**Day 15**
- Core: **Hands-on:** model the Week 2 schema in EF Core with migrations + CRUD, fix an N+1 query, add optimistic concurrency
- Extra: write a couple of unit tests around your repository/DbContext logic

## Week 4: LINQ (Days 16–20)

**Day 16**
- Core: ★ Deferred vs immediate execution
- Extra: SelectMany, Zip, GroupJoin

**Day 17**
- Core: ★ Method vs query syntax; core operators (Select, Where, GroupBy, Join, Aggregate, OrderBy)
- Extra: PLINQ basics and pitfalls; 🆕 `IEnumerator`/`IEnumerable`/`IComparable` — implementing a custom iterator/comparer, how `foreach` actually works under the hood

**Day 18**
- Core: Performance pitfalls; ★ LINQ to Objects vs LINQ to Entities
- Extra: 🆕 `yield return` / `yield break` deep dive — writing custom iterator methods (ties directly into `IEnumerable`)

**Day 19**
- Core: Closures in LINQ, tricky interview questions
- Extra: Expression trees basics (`Expression<Func<T,bool>>`)

**Day 20**
- Core: **Hands-on:** LINQ queries against the EF Core model, including one deliberate deferred-execution bug and fix
- Extra: review Week 1–4 material with self-quiz (write your own interview questions and answer them)

## Week 5: SOLID (Days 21–24)

**Day 21**
- Core: ★ SRP + OCP — code examples
- Extra: DRY, YAGNI, KISS principles

**Day 22**
- Core: LSP + ISP — code examples
- Extra: Law of Demeter, coupling & cohesion

**Day 23**
- Core: ★ DIP — code example, tie to Dependency Injection
- Extra: DI container internals — built-in container vs Autofac/other 3rd-party containers

**Day 24**
- Core: **Hands-on:** refactor a "god class" to comply with all 5 SOLID principles
- Extra: write unit tests for the refactored classes to confirm behavior is unchanged

## Week 6: Design Patterns (Days 25–29)

**Day 25**
- Core: ★ Creational — Singleton, Factory, Builder
- Extra: Prototype pattern, Object Pool pattern

**Day 26**
- Core: Structural — Decorator, Adapter, Facade
- Extra: Proxy pattern, Bridge pattern

**Day 27**
- Core: ★ Behavioral — Strategy, Observer, Mediator (tie to MediatR)
- Extra: Command pattern, Chain of Responsibility, Template Method

**Day 28**
- Core: ★ Repository & CQRS; Clean/Onion Architecture; N-tier vs microservices
- Extra: Event-driven architecture basics, message broker concepts (RabbitMQ/Kafka overview)

**Day 29**
- Core: **Hands-on:** Strategy for a discount engine, Factory for notification types
- Extra: add unit tests covering each pattern implementation

## Week 7: ASP.NET Core Fundamentals (Days 30–35)

**Day 30**
- Core: ★ Request pipeline — middleware, app.Use/Run/Map, order; 🆕 Top-level statements (`Program.cs` minimal hosting model)
- Extra: Hosted services / `IHostedService` / `BackgroundService`

**Day 31**
- Core: ★ DI service lifetimes, captive dependency trap
- Extra: Options pattern validation, named options

**Day 32**
- Core: Configuration — appsettings.json, IOptions variants, secrets management
- Extra: Health checks middleware, writing custom middleware from scratch

**Day 33**
- Core: ★ Minimal API vs Controller-based; routing, route constraints
- Extra: Endpoint routing internals, route template edge cases

**Day 34**
- Core: Filters and execution order; model binding & validation
- Extra: Rate limiting middleware (.NET 7+), output/response caching

**Day 35**
- Core: **Hands-on:** minimal API with custom logging middleware, all 3 service lifetimes, custom action filter
- Extra: add a basic health check endpoint and a rate limiter to the same project

## Week 8: Web API, Security & Auth (Days 36–41)

**Day 36**
- Core: ★ REST principles — verbs, status codes, idempotency, versioning
- Extra: HATEOAS concept, deep dive on versioning strategies (URL vs header vs query string)

**Day 37**
- Core: Controllers, ActionResult<T>, ProblemDetails; API design (pagination, filtering, DTOs, AutoMapper)
- Extra: RFC 7807 Problem Details in depth, content negotiation

**Day 38**
- Core: ★ Swagger/OpenAPI setup; 🆕 XML documentation comments (`///`) and how they power Swagger docs; global exception handling
- Extra: API Gateway pattern (Ocelot/YARP overview — conceptual)

**Day 39**
- Core: CORS; security essentials (HTTPS/HSTS, XSS, CSRF, SQL injection, password hashing)
- Extra: OAuth2 & OpenID Connect concepts, IdentityServer/Duende overview

**Day 40**
- Core: ★ Authentication — cookie auth, JWT, ASP.NET Core Identity
- Extra: Refresh token rotation, token revocation strategies

**Day 41**
- Core: ★ Authorization — role/policy/claims-based, custom handlers
- **Hands-on:** versioned REST API (CRUD) with DTO mapping, global exception handling, Swagger docs, JWT + role-based authorization
- Extra: wire up Swagger UI to support JWT bearer auth for testing

## Week 9: Async, Testing & System Design (Days 42–45)

**Day 42**
- Core: ★ Async/await deep dive; threading basics (Thread vs Task, ThreadPool, lock, race conditions); 🆕 Threading deep dive (synchronization primitives, thread safety)
- Extra: `IAsyncEnumerable`/async streams, `ValueTask` vs `Task`

**Day 43**
- Core: Testing — xUnit, Moq, WebApplicationFactory; resilience (Polly, health checks)
- Extra: BenchmarkDotNet basics, test coverage tooling; 🆕 Serialization in .NET (JSON/XML/binary — System.Text.Json vs Newtonsoft); 🆕 Stream I/O (FileStream, MemoryStream, reading/writing files)

**Day 44**
- Core: ★ Microservices concepts, containerization/Docker, CI/CD concepts; ★ system design practice
- Extra: gRPC basics, pub/sub vs point-to-point messaging, Kubernetes fundamentals (conceptual); 🆕 Assemblies & reflection basics; 🆕 Attributes (built-in and custom); 🆕 NuGet packages & packaging a class library

**Day 45**
- Core: **Hands-on + final review:** add async + cancellation to one endpoint, write unit + integration tests, Dockerize it, sketch one system design on paper
- Extra: full mock interview — talk through your project/resume, practice 2–3 behavioral questions (STAR method), rapid-fire self-quiz on all ★ items across all 9 weeks

---

## What changed from v1 (and why)
The video course covers several C#-language and .NET-ecosystem topics that don't come up in every interview but are worth having ready, especially for "explain X" or take-home-project questions:
- **Enums, Operator Overloading, Tuples, Top-level statements, Strings/StringBuilder** — folded into Week 1 since they're core language basics best learned alongside the rest of C# fundamentals.
- **`IEnumerator`/`IEnumerable`/`IComparable`, `yield`** — moved into Week 4 (LINQ) since they're the mechanics *underneath* LINQ — understanding `yield` makes deferred execution click much faster.
- **Assemblies, Attributes, NuGet packaging, XML docs, Serialization, Stream I/O, Threading depth** — placed in Weeks 8–9 alongside related topics (XML docs → Swagger, threading → async, serialization/streams → testing week) since these are more "ecosystem/tooling" knowledge than core interview drivers — good to know, lower priority if time is tight.

## How to use this
- **Split your 5 hrs:** ~3 hrs Core + ~2 hrs Extra. If a day gets tight, Core always wins, then ★ items within Extra.
- **If you fall behind:** drop 🆕 ecosystem topics (Assemblies, Attributes, NuGet, XML docs) first — they're least likely to be the deciding factor in an interview. Never drop Core or hands-on days.
- **Weekly gut-check:** end each week by explaining that week's ★ topics out loud without notes.
