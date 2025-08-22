## Table of Contents

- [What is Angular?](#what-is-angular)
- [What are Angular components?](#what-are-angular-components)
- [SOLID Principles in C#](#solid-principles-in-c)
- [Singleton Pattern](#singleton-pattern)
- [Factory Pattern](#factory-pattern)
- [Repository Pattern](#repository-pattern)
- [Observer Pattern](#observer-pattern)
- [Strategy Pattern](#strategy-pattern)
- [Dependency Injection Pattern](#dependency-injection-pattern)
- [Adapter Pattern](#adapter-pattern)
- [Decorator Pattern](#decorator-pattern)
- [Command Pattern](#command-pattern)
- [Mediator Pattern](#mediator-pattern)
- [C# 13 Latest Features](#c-13-latest-features)
- [Angular 20 New Features](#angular-20-new-features)
- [Top 10 RxJS Functions in Angular](#top-10-rxjs-functions-in-angular)

---

<details>
<summary id="what-is-angular">What is Angular?</summary>

Angular is a TypeScript-based open-source web application framework led by the Angular Team at Google.

</details>

<details>
<summary id="what-are-angular-components">What are Angular components?</summary>

Components are the basic building blocks of Angular applications. They control a part of the UI and consist of an HTML template, a TypeScript class, and CSS styles.

</details>

<details>
<summary id="solid-principles-in-c">SOLID Principles in C#</summary>

**S**: Single Responsibility Principle – A class should have only one reason to change.  
**O**: Open/Closed Principle – Software entities should be open for extension but closed for modification.  
**L**: Liskov Substitution Principle – Subtypes must be substitutable for their base types.  
**I**: Interface Segregation Principle – No client should be forced to depend on methods it does not use.  
**D**: Dependency Inversion Principle – Depend on abstractions, not concretions.

</details>

<details>
<summary id="singleton-pattern">Singleton Pattern</summary>

Ensures only one instance of a class exists and provides a global point of access.

```csharp
public sealed class Singleton {
    private static readonly Singleton instance = new Singleton();
    private Singleton() {}
    public static Singleton Instance => instance;
}
```
</details>

<details>
<summary id="factory-pattern">Factory Pattern</summary>

Creates objects without specifying the exact class of object that will be created.

```csharp
public interface IProduct { }
public class ProductA : IProduct { }
public class ProductB : IProduct { }
public class Factory {
    public static IProduct GetProduct(string type) {
        return type == "A" ? new ProductA() : (IProduct)new ProductB();
    }
}
```
</details>

<details>
<summary id="repository-pattern">Repository Pattern</summary>

Abstracts the data layer, providing a collection-like interface for accessing domain objects.

</details>

<details>
<summary id="observer-pattern">Observer Pattern</summary>

Defines a one-to-many dependency so that when one object changes state, all its dependents are notified.

**Example:**  
Events/delegates in C# are commonly used for this.

</details>

<details>
<summary id="strategy-pattern">Strategy Pattern</summary>

Defines a family of algorithms, encapsulates each one, and makes them interchangeable.

</details>

<details>
<summary id="dependency-injection-pattern">Dependency Injection Pattern</summary>

A technique where an object receives its dependencies from an external source rather than creating them itself. Widely used in ASP.NET Core with built-in DI container.

</details>

<details>
<summary id="adapter-pattern">Adapter Pattern</summary>

Allows incompatible interfaces to work together.

</details>

<details>
<summary id="decorator-pattern">Decorator Pattern</summary>

Adds new behaviors to objects dynamically by placing them inside special wrapper objects.

</details>

<details>
<summary id="command-pattern">Command Pattern</summary>

Encapsulates a request as an object, thereby allowing for parameterization and queuing of requests.

</details>

<details>
<summary id="mediator-pattern">Mediator Pattern</summary>

Defines an object that encapsulates how a set of objects interact, promoting loose coupling.

</details>

<details>
<summary id="c-13-latest-features">C# 13 Latest Features</summary>

**C# 13 (2025) Notable Features:**
1. **Primary Constructors for All Types:** Use primary constructors in any type (not just records).
   ```csharp
   public class Person(string name, int age) {
       public string Name { get; } = name;
       public int Age { get; } = age;
   }
   ```
2. **Collection Literals:** New syntax for easily creating collections.
   ```csharp
   var numbers = [1, 2, 3];
   ```
3. **Parameter Null-Checking Simplification:** Use the `!!` operator in parameter lists to auto-check for nulls.
   ```csharp
   void Save(string name!!) { ... }
   ```
4. **Lambda Expressions with Params**
5. **Better Pattern Matching Enhancements**
6. **Extension Types (Preview)**
7. **Required Members for Structs**
8. **Improved Interpolated String Handlers**
9. **Experimental Features Toggle**
10. **Other Minor Improvements**

</details>

<details>
<summary id="angular-20-new-features">Angular 20 New Features</summary>

**Angular 20 (2024) Key Features:**
- Full Standalone API Support (no NgModules required)
- Default Standalone Projects in CLI
- Signal-based Components (Stable)
- New Control Flow Syntax (`@for`, `@if`, `@switch`)
- Deferred Loading (`@defer`)
- "Destroyed" Lifecycle Hook for signals
- Improved SSR and Hydration
- New Testing APIs
- Smaller Bundle Sizes
- Updated dependencies (TypeScript, RxJS, Zone.js)
- Standalone Angular Router

</details>

<details>
<summary id="top-10-rxjs-functions-in-angular">Top 10 RxJS Functions in Angular</summary>

1. **Observable** – The core class; creates and manages streams of data.
2. **Subject / BehaviorSubject / ReplaySubject** – Special types for multicasting and state management.
3. **map** – Transforms emitted values.
4. **filter** – Emits only values that pass a condition.
5. **switchMap** – Switches to a new Observable, cancelling previous ones.
6. **mergeMap (flatMap)** – Flattens all inner Observables.
7. **catchError** – Handles errors in the observable stream.
8. **debounceTime** – Delays emitted values based on time.
9. **take / takeUntil** – Emits only the first N values or until another observable emits.
10. **combineLatest / forkJoin / zip** – Combines multiple Observables into one.

</details>
