# Object-Oriented Programming (OOP) in Java

## Status
- **Overall Level**: 3/5
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5
- **Confidence**: High

## What I Have Learned
- **Core OOP Pillars**:
  - **Encapsulation**: Private fields, public getters and setters, hiding internal state.
  - **Inheritance**: Subclassing with `extends`, single inheritance in Java, `super` keyword, method overriding (`@Override`).
  - **Polymorphism**: Dynamic method dispatch, method overloading (compile-time polymorphism) vs method overriding (runtime polymorphism).
  - **Abstraction**: Abstract classes (`abstract class`), abstract methods (`abstract void method()`), Interfaces (`interface`, `implements`), multiple interface implementation.
- **Class Structure & Modeling**:
  - Constructors (default, parameterized, overloading constructors).
  - UML Class Diagrams: Drawing and interpreting class relationships (Association, Aggregation, Composition, Inheritance).
  - Special Object Methods: `toString()`, `equals()` and `hashCode()` contract.
  - Packages & Access Control: `public`, `protected`, default (package-private), `private`.
- **OOP Exercises**:
  - Book Management system (Author, Price, Release Year).
  - Movie Management system (Manufacturer, Ticket price, Release date).
  - Student Management system (ID, Name, Date of Birth, Average Score, Rank).
  - Computer Management system (Manufacturer, Country, Price, Warranty).

## What I Understand
- **Encapsulation**: Why variables should be encapsulated to protect invariants and prevent unauthorized direct state modification.
- **Inheritance & Polymorphism**: How dynamic binding works at runtime, calling base class constructors via `super()`, and why Java enforces single class inheritance (diamond problem prevention).
- **Interface vs Abstract Class**: When to use an abstract class (is-a relationship, shared code/state) versus an interface (can-do contract, multiple inheritance of type).
- **Equals & HashCode Contract**: Why overriding `equals()` requires overriding `hashCode()` when objects are stored in Hash-based collections (`HashMap`, `HashSet`).

## What I Can Do
- Model real-world entities into Java classes with encapsulated fields, constructors, getters/setters, and methods.
- Design inheritance hierarchies using base classes, abstract classes, and interfaces.
- Implement comparator methods (`compareTo`, `equals`) for domain entities.
- Read UML diagrams and translate them into Java code structures.

## What I Cannot Yet Do
- Apply advanced Design Patterns (SOLID principles, GoF patterns like Factory, Observer, Strategy, Singleton, Builder, Adapter) in production architectures.
- Refactor legacy monolithic codebases into decoupled, modular OOP components.
- Analyze trade-offs of Composition vs Inheritance in complex domain-driven designs.

## Sources & Knowledge Traceability

**Knowledge $\rightarrow$ Source Mapping**:
- **SRC-001** — Lập trình Java – Java Core (TITV) | URL: https://titv.vn/courses-page/lap-trinh-java-java-core/ | Lessons 28-48 (OOP Pillars, UML, Abstract, Interface)

Master Sources Catalog: [`00-sources/learning-sources.md`](../00-sources/learning-sources.md)

## Weaknesses
- Limited exposure to SOLID principles (Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion).
- Minimal hands-on experience applying design patterns to software projects.

## Missing Knowledge
- SOLID Design Principles in Java.
- Gang of Four (GoF) Design Patterns.
- Domain-Driven Design (DDD) fundamentals.

## Recommended Supplement
1. Study SOLID principles with concrete Java examples.
2. Implement 5 key Design Patterns in Java (Singleton, Factory, Builder, Strategy, Observer).
