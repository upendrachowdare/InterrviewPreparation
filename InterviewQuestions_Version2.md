## Table of Contents

- [Angular Interview Questions](#angular-interview-questions)
- [C# Interview Questions](#c-interview-questions)
- [Other JavaScript Questions](#other-javascript-questions)
- [Design Patterns](#design-patterns)
- [SOLID Principles](#solid-principles)
- [Latest Features](#latest-features)

---

# Angular Interview Questions
[Back to Top](#table-of-contents)

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

[Back to Top](#table-of-contents)

---

# C# Interview Questions
[Back to Top](#table-of-contents)

<details>
<summary>Table of Contents</summary>

- [What is C#?](#what-is-c)
- [What are value types and reference types in C#?](#what-are-value-types-and-reference-types-in-c)
- [How does garbage collection work in C#?](#how-does-garbage-collection-work-in-c)
- [What is Finalize and Destructor in C#? What’s the main difference?](#what-is-finalize-and-destructor-in-c-what-is-the-main-difference)
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
<summary id="how-does-garbage-collection-work-in-c">How does garbage collection work in C#?</summary>

**Garbage Collection (GC)** in C# is an automatic memory management feature. It automatically finds objects that are no longer used by the application and reclaims their memory.  
Key points:
- The .NET GC runs on the managed heap and tracks object references.
- When there’s not enough memory, the GC pauses the application and checks for unreachable (unused) objects.
- It frees up memory taken by objects with no references.
- GC uses generations (0, 1, and 2) to optimize collection. Short-lived objects are collected more often (Gen 0), while long-lived ones are promoted to higher generations.
- You can force GC with `GC.Collect()`, but it's not recommended unless necessary.

</details>

<details>
<summary id="what-is-finalize-and-destructor-in-c-what-is-the-main-difference">What is Finalize and Destructor in C#? What’s the main difference?</summary>

**Finalize:**  
- The `Finalize` method allows an object to clean up unmanaged resources before it is collected by the garbage collector.
- You implement it by defining a finalizer in C#:  
  ```csharp
  ~MyClass() {
      // cleanup code
  }
  ```
- The runtime translates the destructor syntax into an override of the `Object.Finalize` method.
- `Finalize` is called automatically by the GC, not by your code.

**Destructor:**  
- In C#, the destructor (`~MyClass`) is a special method that the compiler translates to a `Finalize` override.
- You cannot call a destructor directly; it's triggered by the GC.

**Main Differences:**  
- Destructor is C# syntax; Finalize is the actual method in the .NET base class.
- You cannot control exactly when the destructor/finalizer runs; it runs non-deterministically after the object becomes unreachable.
- Finalizers are used to release unmanaged resources, but using `IDisposable` and the `Dispose` method (with a `using` statement) is preferred for deterministic cleanup.
- Relying on finalizers can delay resource release and impact performance.

**Best Practice:**  
- Use destructors/finalizers only when absolutely necessary (unmanaged resources).
- Prefer implementing the `IDisposable` pattern for releasing resources.

</details>

<details>
<summary id="solid-principles-in-c">SOLID Principles in C# (Simple Understanding & Example)</summary>

**S: Single Responsibility Principle (SRP)**  
*A class should have only one reason to change (one job or responsibility).*

```csharp
// BAD: Both logic and saving data in one class
public class Report {
    public string Text { get; set; }
    public void SaveToFile(string path) {
        // File save logic
    }
}

// GOOD: Split into separate classes
public class Report {
    public string Text { get; set; }
}
public class ReportSaver {
    public void SaveToFile(Report report, string path) {
        // File save logic
    }
}
```

---

**O: Open/Closed Principle (OCP)**  
*Software entities (classes, methods, etc.) should be open for extension, but closed for modification.*

```csharp
// BAD: Add new shape types by modifying existing code
public class AreaCalculator {
    public double Area(object shape) {
        if (shape is Rectangle rect)
            return rect.Width * rect.Height;
        if (shape is Circle circ)
            return Math.PI * circ.Radius * circ.Radius;
        // More shapes...
        throw new NotSupportedException();
    }
}

// GOOD: Use inheritance and polymorphism
public abstract class Shape {
    public abstract double Area();
}
public class Rectangle : Shape {
    public double Width, Height;
    public override double Area() => Width * Height;
}
public class Circle : Shape {
    public double Radius;
    public override double Area() => Math.PI * Radius * Radius;
}
public class AreaCalculator {
    public double Area(Shape shape) => shape.Area();
}
```

---

**L: Liskov Substitution Principle (LSP)**  
*Derived classes must be substitutable for their base classes without breaking the behavior.*

```csharp
// BAD: Square breaks Rectangle's behavior
public class Rectangle {
    public virtual int Width { get; set; }
    public virtual int Height { get; set; }
}
public class Square : Rectangle {
    public override int Width { set { base.Width = base.Height = value; } }
    public override int Height { set { base.Width = base.Height = value; } }
}

// GOOD: Avoid inheritance if not a true "is-a" relationship
// Separate classes or use interfaces, if necessary
```

---

**I: Interface Segregation Principle (ISP)**  
*Clients should not be forced to depend on interfaces they do not use.*

```csharp
// BAD: Fat interface
public interface IWorker {
    void Work();
    void Eat();
}
public class Robot : IWorker {
    public void Work() { /* ... */ }
    public void Eat() { /* Not needed, but must implement */ }
}

// GOOD: Split into smaller interfaces
public interface IWorkable { void Work(); }
public interface IEatable { void Eat(); }
public class Robot : IWorkable {
    public void Work() { /* ... */ }
}
public class Human : IWorkable, IEatable {
    public void Work() { /* ... */ }
    public void Eat() { /* ... */ }
}
```

---

**D: Dependency Inversion Principle (DIP)**  
*Depend on abstractions, not on concrete implementations.*

```csharp
// BAD: High-level module depends on low-level class
public class FileLogger {
    public void Log(string message) { /* ... */ }
}
public class AuthService {
    private FileLogger _logger = new FileLogger();
    public void Login(string user) { _logger.Log("User logged in"); }
}

// GOOD: Depend on abstraction (interface)
public interface ILogger {
    void Log(string message);
}
public class FileLogger : ILogger {
    public void Log(string message) { /* ... */ }
}
public class AuthService {
    private ILogger _logger;
    public AuthService(ILogger logger) { _logger = logger; }
    public void Login(string user) { _logger.Log("User logged in"); }
}
```

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

[Back to Top](#table-of-contents)

---

# Other JavaScript Questions
[Back to Top](#table-of-contents)

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

[Back to Top](#table-of-contents)

---

# Design Patterns
[Back to Top](#table-of-contents)

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

[Back to Top](#table-of-contents)

---

# SOLID Principles
[Back to Top](#table-of-contents)

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

[Back to Top](#table-of-contents)

---

# Latest Features
[Back to Top](#table-of-contents)

<details>
<summary>Angular 20 New Features</summary>
(see Angular section)
</details>
<details>
<summary>C# 13 Latest Features</summary>
(see C# section)
</details>

[Back to Top](#table-of-contents)
