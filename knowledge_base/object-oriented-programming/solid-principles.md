# SOLID Principles

> Phase 1.1 | Status: Partial | Priority: HIGH

## Current Knowledge

- Applied in .NET projects but need to formalize understanding
- Can recognize violations but need to articulate the "why" better
- See also: general-concepts.md for initial notes

## Examples / Notes

### Single Responsibility Principle (SRP)
- A class should have only one reason to change
- TODO: Add C# examples of SRP violation and fix

### Open/Closed Principle (OCP)
- Open for extension, closed for modification
- TODO: Strategy pattern as OCP implementation

### Liskov Substitution Principle (LSP)
- Subtypes must be substitutable for their base types
- TODO: Classic Rectangle/Square violation example

### Interface Segregation Principle (ISP)
- Clients should not depend on interfaces they don't use
- TODO: Fat interface example and how to split it

### Dependency Inversion Principle (DIP)
- Depend on abstractions, not concretions
- TODO: Example with AutoFac (used in FIS project)

## Questions / Confusions

- How do SOLID principles interact with each other? (e.g., SRP + ISP overlap)
- When does following SOLID become over-engineering?
- How to apply SOLID in Angular/TypeScript vs C#?
