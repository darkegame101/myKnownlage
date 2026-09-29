# Domain: Programming (Java) — Summary

## Current Level
- **Overall**: 3/5
- **Theory**: 3/5
- **Practical**: 2/5
- **Troubleshooting**: 1/5
- **Design**: 2/5

## What I Have Learned
- Core Java syntax, primitive and reference types, type casting, arithmetic/logical operations.
- Control flow structures (`if-else`, `switch-case`, `for`, `while`, `do-while`, `break`, `continue`).
- OOP fundamentals: Encapsulation, Inheritance, Polymorphism, Abstraction, Interfaces, Abstract classes.
- Java Collections Framework (`ArrayList`, `Stack`, `Queue`, `Set`, `Map`, Generics).
- Exception handling (`try-catch-finally`).
- File I/O, Character/Byte Streams, Object Serialization, Zip compression.
- Desktop GUI development using Java Swing (JFrame, JPanel, Layouts, Events, MVC).
- Project build management using Apache Maven (`pom.xml`, GAV coordinates, dependency resolution, packaging `.jar`/`.war`, multi-module hierarchy, running automated tests).
- Modern Java 8+ features: Lambda expressions (`->`), functional interfaces, Streams API (`filter`, `map`, `flatMap`, `distinct`, `sorted`, `collect`), and `Optional<T>` NPE prevention.

## Strong Areas
- Object-Oriented Class modeling, encapsulation, and inheritance implementation.
- Basic Java standard library usage (Math, Arrays, Collections, File handling).
- Basic GUI construction using Java Swing.
- Standard Maven project configuration, dependency management, and multi-module structuring.
- Modern Java 8+ functional syntax: Lambda expressions, collection data transformation with Streams API, and safe handling with `Optional`.

## Weak Areas
- Multi-threading & Concurrency utilities (`java.util.concurrent`, Parallel Streams thread-safety).
- Unit Testing (JUnit 5, Mockito depth) & Advanced Maven CLI / CI integration.

## Missing Knowledge
- **Advanced Build & CI**: Gradle, advanced Maven plugins (Shade, Assembly), GitHub Actions Maven CI pipeline.
- **Advanced Functional Programming**: Custom Stream Collectors (`Collector.of`), Parallel Streams performance tuning, primitive streams (`IntStream`).
- **Unit Testing**: JUnit 5 test suites, AssertJ, Mockito mocking framework.
- **SOLID Principles & Design Patterns**: Creational, Structural, and Behavioral patterns.

## Practical Gaps
- Theory Known: Java OOP, Swing, Maven & Java 8 Streams = 3/5.
- Practical Known: Standard exercises, Maven builds & Stream pipelines = 3/5.
- Gap: No production backend project (e.g. Spring Boot REST API with Maven/Gradle).

## Depth Gaps
- Exception Handling: Learned `try-catch`, missing custom business exceptions, global exception handling, runtime vs checked exception strategy.
- Java Collections: Learned standard collections, missing internal hash collision resolution mechanisms (LinkedList bucket vs Red-Black tree in HashMap Java 8).

## Recommended Supplements
1. **Testing**: Write JUnit 5 test suites with assertions for Java domain logic.
2. **Spring Boot Core**: Ready to explore Spring Boot DI / IoC container and REST controllers.
3. **Maven CLI**: Practice building and packaging from terminal without IDE.

## Readiness
- **Backend Development (Spring Boot)**: **ALMOST READY**
  - Java Core: 3/5
  - OOP: 3/5
  - Java Collections: 3/5
  - Maven: **3/5 (READY)**
  - Java 8 Streams & Lambdas: **3/5 (READY)**
  - Unit Testing: 1/5
  - *Action*: Practice basic JUnit 5 assertions and understand DI before jumping into Spring Boot.


