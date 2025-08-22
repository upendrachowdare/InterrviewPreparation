## Table of Contents

- [Angular Interview Questions](#angular-interview-questions)
- [C# Interview Questions](#c-interview-questions)
- [Other JavaScript Questions](#other-javascript-questions)
- [Design Patterns](#design-patterns)
- [SOLID Principles](#solid-principles)
- [Latest Features](#latest-features)

---

# Angular Interview Questions
<details>
<summary>Table of Contents</summary>

- [What is Angular?](#what-is-angular)
- [What are Angular components?](#what-are-angular-components)
- [Angular 20 New Features](#angular-20-new-features)
- [Top 10 RxJS Functions in Angular](#top-10-rxjs-functions-in-angular)
</details>

<details>
<summary id="what-is-angular">What is Angular?</summary>
Angular is a TypeScript-based open-source web application framework led by the Angular Team at Google.
</details>

<details>
<summary id="what-are-angular-components">What are Angular components?</summary>
Components are the basic building blocks of Angular applications. They control a part of the UI and consist of an HTML template, a TypeScript class, and CSS styles.
</details>

<details>
<summary id="angular-20-new-features">Angular 20 New Features</summary>
<ul>
<li>Full Standalone API Support (no NgModules required)</li>
<li>Default Standalone Projects in CLI</li>
<li>Signal-based Components (Stable)</li>
<li>New Control Flow Syntax (@for, @if, @switch)</li>
<li>Deferred Loading (@defer)</li>
<li>"Destroyed" Lifecycle Hook for signals</li>
<li>Improved SSR and Hydration</li>
<li>New Testing APIs</li>
<li>Smaller Bundle Sizes</li>
<li>Updated dependencies (TypeScript, RxJS, Zone.js)</li>
<li>Standalone Angular Router</li>
</ul>
</details>

<details>
<summary id="top-10-rxjs-functions-in-angular">Top 10 RxJS Functions in Angular</summary>
1. Observable  
2. Subject / BehaviorSubject / ReplaySubject  
3. map  
4. filter  
5. switchMap  
6. mergeMap (flatMap)  
7. catchError  
8. debounceTime  
9. take / takeUntil  
10. combineLatest / forkJoin / zip  
</details>

---

# C# Interview Questions
<details>
<summary>Table of Contents</summary>

- [What is C#?](#what-is-c)
- [What are value types and reference types in C#?](#what-are-value-types-and-reference-types-in-c)
- [SOLID Principles in C#](#solid-principles-in-c)
- [C# 13 Latest Features](#c-13-latest-features)
</details>

<details>
<summary id="what-is-c">What is C#?</summary>
C# is a modern, object-oriented programming language developed by Microsoft for the .NET platform.
</details>

<details>
<summary id="what-are-value-types-and-reference-types-in-c">What are value types and reference types in C#?</summary>
Value types store data directly (e.g., int, struct), while reference types store references to data (e.g., class, interface).
</details>

<details>
<summary id="solid-principles-in-c">SOLID Principles in C#</summary>
S: Single Responsibility Principle  
O: Open/Closed Principle  
L: Liskov Substitution Principle  
I: Interface Segregation Principle  
D: Dependency Inversion Principle  
</details>

<details>
<summary id="c-13-latest-features">C# 13 Latest Features</summary>
<ul>
<li>Primary Constructors for All Types</li>
<li>Collection Literals</li>
<li>Parameter Null-Checking Simplification (!! operator)</li>
<li>Lambda Expressions with Params</li>
<li>Better Pattern Matching Enhancements</li>
<li>Extension Types (Preview)</li>
<li>Required Members for Structs</li>
<li>Improved Interpolated String Handlers</li>
<li>Experimental Features Toggle</li>
<li>Other Minor Improvements</li>
</ul>
</details>

---

# Other JavaScript Questions
<details>
<summary>Table of Contents</summary>

- [What is JavaScript?](#what-is-javascript)
- [Explain event delegation in JavaScript.](#explain-event-delegation-in-javascript)
- [Explain closures in JavaScript.](#explain-closures-in-javascript)
</details>

<details>
<summary id="what-is-javascript">What is JavaScript?</summary>
JavaScript is a high-level, interpreted programming language used for web development to make web pages interactive.
</details>

<details>
<summary id="explain-event-delegation-in-javascript">Explain event delegation in JavaScript.</summary>
Event delegation is a technique where a single event handler is added to a parent element to handle events for child elements, improving performance and code maintainability.
</details>

<details>
<summary id="explain-closures-in-javascript">Explain closures in JavaScript.</summary>
A closure is a function that has access to its own scope, the scope of the outer function, and the global scope.
</details>

---

# Design Patterns
<details>
<summary>Table of Contents</summary>

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

---

# SOLID Principles
<details>
<summary id="solid-principles">What are SOLID Principles?</summary>
SOLID is an acronym representing five key object-oriented design principles to make software designs more understandable, flexible, and maintainable:
<ul>
<li>Single Responsibility Principle</li>
<li>Open/Closed Principle</li>
<li>Liskov Substitution Principle</li>
<li>Interface Segregation Principle</li>
<li>Dependency Inversion Principle</li>
</ul>
</details>

---

# Latest Features
<details>
<summary>Angular 20 New Features</summary>
(see Angular section)
</details>
<details>
<summary>C# 13 Latest Features</summary>
(see C# section)
</details>
