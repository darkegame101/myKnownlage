# Modern Java 8+ Features: Streams API, Lambdas & Optional

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5
- **Confidence**: Medium

## What I Have Learned
- **Lambda Expressions (`->`)**:
  - Syntax: `(parameters) -> expression` and `(parameters) -> { statements; }`.
  - Type inference in parameters and single-statement expression returns.
  - Functional Interfaces: Single Abstract Method (SAM) interfaces, `@FunctionalInterface` annotation.
- **Streams API**:
  - Processing pipeline structure: Data Source $\rightarrow$ Intermediate Operations (lazy) $\rightarrow$ Terminal Operation (eager).
  - Intermediate operations: `filter(Predicate)`, `map(Function)`, `flatMap()`, `distinct()`, `sorted()`, `limit()`.
  - Terminal operations: `collect(Collectors.toList())`, `collect(Collectors.toSet())`, `count()`, `min()`, `max()`, `reduce()`, `forEach()`, `toArray()`.
- **`Optional<T>` Wrapper**:
  - Prevention of `NullPointerException` (NPE).
  - Creation: `Optional.empty()`, `Optional.of(val)`, `Optional.ofNullable(val)`.
  - Unwrapping & Handling: `.isPresent()`, `.isEmpty()`, `.orElse(defaultVal)`, `.orElseGet(Supplier)`, `.orElseThrow(Supplier)`.
  - Functional transformation: `.map()`, `.filter()` on Optional containers.

## What I Understand
- Why Java introduced functional programming concepts in Java 8: shifting from imperative (telling the computer step-by-step *how* to do work via loops) to declarative (specifying *what* data to transform).
- Difference between Collections (in-memory data structure holding elements) and Streams (computational channel that traverses and processes elements on-demand).
- Mechanism of Lazy Evaluation: Intermediate operations are not executed until a terminal operation is called on the stream.
- How `Optional` serves as a type-level contract indicating that a method return value may be absent, eliminating defensive `if (x != null)` cascades.

## What I Can Do
- Replace verbose anonymous inner classes with concise lambda expressions.
- Filter, map, sort, and collect collection items using Java Stream pipelines.
- Transform data lists between Entity objects and DTO models using `.map()`.
- Wrap potentially absent return types in `Optional<T>` and retrieve them safely using `.orElseThrow(() -> new BusinessException(...))`.

## What I Cannot Yet Do
- Optimize performance using Parallel Streams (`parallelStream()`) while safely avoiding thread-safety issues in shared mutable state.
- Implement custom `Collector` interfaces via `Collector.of(...)` for complex aggregation logic.
- Master all built-in functional interfaces in `java.util.function` (`BiPredicate`, `UnaryOperator`, `BinaryOperator`) and complex currying.
- Optimize high-throughput data pipelines using primitive streams (`IntStream`, `LongStream`, `DoubleStream`) to avoid autoboxing overhead.

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-010** — Biểu thức Lambda cực dễ hiểu (Code Thu) | URL: https://www.youtube.com/watch?v=dKzTdBXgHsg
  - Evidence Record: [`00-sources/C010-java-lambda.md`](../00-sources/C010-java-lambda.md)
- **SRC-011** — Java Streams Tutorial Series (SDET-QA) | URL: https://www.youtube.com/playlist?list=PLUDwpEzHYYLvTPVqVIt7tlBohABLo4gyg
  - Evidence Record: [`00-sources/C011-java-streams.md`](../00-sources/C011-java-streams.md)
- **SRC-012** — Optionals In Java - Simple Tutorial (Coding with John) | URL: https://www.youtube.com/watch?v=vKVzRbsMnTQ
  - Evidence Record: [`00-sources/C012-java-optional.md`](../00-sources/C012-java-optional.md)

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Limited hands-on experience debugging stack traces originating from nested stream pipelines or method references.
- Potential temptation to overuse Streams for trivial loops where simple `for-each` is more readable.

## Missing Knowledge
- **Advanced Stream Collectors**: `Collectors.groupingBy()`, `Collectors.partitioningBy()`, downstream collectors.
- **Method References**: Advanced syntax (`ClassName::methodName`, `this::methodName`, `SuperClass::methodName`, constructor references `Class::new`).
- **Parallel Streams & ForkJoinPool**: Multi-core stream processing and thread-pool configuration.

## Recommended Supplements
1. Practice writing Stream data transformations on real-world datasets (e.g. products, orders).
2. Integrate `Optional` return types into DAO / Repository data access layers.
