# Course Summary: C012 — Optionals in Java Tutorial

## Course Overview
- **Course ID**: C012
- **Provider**: Coding with John (YouTube)
- **Course Name**: Optionals In Java - Simple Tutorial
- **URL**: [https://www.youtube.com/watch?v=vKVzRbsMnTQ](https://www.youtube.com/watch?v=vKVzRbsMnTQ)
- **Status**: Completed
- **Total Lectures**: 1 Video Tutorial

## Topics Covered
1. **The Null Problem**: Why returning `null` leads to unexpected `NullPointerException` runtime errors.
2. **`Optional<T>` Container Concept**: Wrapping a value that might or might not be present; treating missing values as explicit types.
3. **Creating Optionals**:
   - `Optional.empty()`: Explicitly empty container.
   - `Optional.of(value)`: Non-null container (throws NPE if null).
   - `Optional.ofNullable(value)`: Safely accepts null or non-null values.
4. **Consuming Optionals**:
   - `.isPresent()` and `.isEmpty()`.
   - `.get()` (and why raw `.get()` should usually be avoided).
   - `.orElse(defaultValue)`: Fallback value if absent.
   - `.orElseGet(Supplier)`: Lazy evaluation of default value.
   - `.orElseThrow(Supplier)`: Explicitly throwing business exceptions when value is absent (core Spring Boot pattern).
   - `.map()` and `.filter()` over Optionals.

## Topics Already Known Before Course
- Java Reference types and `null` checking using `if (obj != null)`.
- Exception throwing and custom exceptions.

## New Knowledge Added
- `java.util.Optional<T>` API and method chaining.
- Eliminating defensive null checks in service layer code.
- Functional exception throwing via `.orElseThrow(() -> new NotFoundException(...))`.

## Knowledge Deepened
- API design contract: indicating to callers that a method's return value may be absent.

## Practical Skills Added
- Wrapping database and service method return types in `Optional<T>`.
- Using `.orElseThrow()` to throw expressive domain exceptions.

## Remaining Gaps
- Anti-patterns in Optional usage: using Optional as method parameters, serializing Optionals, or wrapping collections in Optional (should return empty collection instead).
- `OptionalDouble`, `OptionalInt`, `OptionalLong` primitive specializations.

## Resulting Skill Level
- **Theory**: 3/5
- **Practical**: 3/5
- **Troubleshooting**: 2/5
- **Design**: 2/5

## Recommended Follow-up
- Apply `Optional` in Spring Data JPA repository methods (e.g. `findById`).
- Combine `Optional` with custom business exceptions in backend service layers.
