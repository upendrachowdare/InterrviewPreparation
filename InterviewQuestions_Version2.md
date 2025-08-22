# Interview Questions Collection

A curated list of interview questions for quick preparation. Feel free to add your own questions and answers!

---

## Angular Interview Questions

### 1. What is Angular?
Angular is a TypeScript-based open-source web application framework led by the Angular Team at Google.

### 2. What are Angular components?
Components are the basic building blocks of Angular applications. They control a part of the UI and consist of an HTML template, a TypeScript class, and CSS styles.

### 3. Explain data binding in Angular.
Data binding is the process that allows data to flow between the component class and its template. Angular supports one-way and two-way data binding.

### 4. What are directives in Angular?
Directives are classes that add behavior to elements in Angular applications. They come in three types: component, structural, and attribute directives.

### 5. What is dependency injection in Angular?
Dependency Injection (DI) is a design pattern in which an object receives other objects it depends on. Angular’s DI framework provides dependencies to components and services.

### 6. What is a service in Angular?
A service is a class with a specific purpose, such as fetching data or business logic, that can be shared across components.

### 7. How does Angular handle forms?
Angular supports template-driven and reactive forms, providing validation and data management mechanisms.

### 8. What is RxJS and how is it used in Angular?
RxJS is a library for reactive programming using Observables. Angular heavily uses RxJS for handling asynchronous operations.

---

#### Top 10 Commonly Used RxJS Functions/Operators in Angular

1. **Observable**  
   The core class; creates and manages streams of data.

2. **Subject / BehaviorSubject / ReplaySubject**  
   Special types of Observables for multicasting and state management.

3. **map**  
   Transforms emitted values.

4. **filter**  
   Emits only values that pass a condition.

5. **switchMap**  
   Switches to a new Observable when a new value is emitted, cancelling previous inner Observables.

6. **mergeMap (flatMap)**  
   Maps each value to an Observable, then flattens all inner Observables.

7. **catchError**  
   Catches errors on the Observable to handle or rethrow them.

8. **debounceTime**  
   Emits a value from the source Observable only after a particular time span has passed without another source emission.

9. **take / takeUntil**  
   Emits only the first N values (take) or until another Observable emits (takeUntil).

10. **combineLatest / forkJoin / zip**  
    Combines multiple Observables into one.

---

### 9. What is Angular CLI?
Angular CLI is a command-line interface tool that helps to initialize, develop, scaffold, and maintain Angular applications.

### 10. What is change detection in Angular?
Change detection is the mechanism that Angular uses to track changes to data and update the view accordingly.

### 11. What are pipes in Angular?
Pipes are used to transform data in templates. Angular provides built-in pipes, and you can create custom ones.

### 12. How do you create a custom pipe?
Implement the PipeTransform interface and add the @Pipe decorator to your class.

### 13. What is lazy loading in Angular?
Lazy loading is a design pattern that loads feature modules only when they are required, improving performance.

### 14. What is the difference between ngOnInit and constructor?
The constructor is used for dependency injection, while ngOnInit is a lifecycle hook called after the component’s data-bound properties have been initialized.

### 15. How does Angular routing work?
Angular’s RouterModule enables navigation among different views and supports route guards, lazy loading, and route parameters.

---

### Angular 20 New Features (2024)

- **Full Standalone API Support**: All Angular APIs (including HttpClient, forms, router, pipes, etc.) now support Standalone Components and do not require NgModules.
- **Default Standalone Projects**: The Angular CLI generates standalone apps and libraries by default.
- **Signal-based Components (Stable)**: Angular's new reactive state primitive, signals, are now stable and recommended for fine-grained reactivity.
- **Control Flow Syntax**: The new built-in control flow (like `@for`, `@if`, `@switch` directives) replaces legacy `*ngFor` and `*ngIf` in templates for better performance and DX.
- **Deferred Loading (`@defer`)**: Built-in deferred loading for rendering content asynchronously, improving Core Web Vitals and user experience.
- **Destroyed Lifecycle Hook**: New `ngOnDestroy`-like "destroyed" signal is available for better cleanup in reactive components.
- **Improved SSR (Server Side Rendering)**: Hydration is enabled by default and more robust.
- **Better Testing APIs**: New `TestBed` APIs and utilities for easier component and signal testing.
- **Smaller Bundle Sizes**: Tree-shaking and build optimizations reduce JavaScript bundle sizes.
- **Updated Dependency Versions**: Updated to latest TypeScript, RxJS, and Zone.js versions.
- **Reworked Router**: The Angular Router is now fully standalone, works with signals, and supports new control flow syntax.

---

## C# Interview Questions

### 31. What is C#?
C# is a modern, object-oriented programming language developed by Microsoft for the .NET platform.

### 32. What are value types and reference types in C#?
Value types store data directly (e.g., int, struct), while reference types store references to data (e.g., class, interface).

### 33. Explain the difference between an interface and an abstract class.
An abstract class can provide method implementations and fields, while an interface only declares methods and properties (since C# 8.0, interfaces can have default implementations).

### 34. What is the difference between ‘==’ and ‘Equals()’ in C#?
‘==’ is an operator that can be overloaded for value or reference equality, while ‘Equals()’ is a method that checks for value equality.

### 35. What is LINQ?
Language Integrated Query (LINQ) is a feature for querying data from different sources using C# syntax.

### 36. What are delegates in C#?
Delegates are type-safe function pointers used to encapsulate methods and support events and callbacks.

### 37. What is an event in C#?
An event is a message sent by an object to signal the occurrence of an action. Events use delegates under the hood.

### 38. What is exception handling in C#?
Exception handling uses try, catch, finally, and throw keywords to handle runtime errors gracefully.

### 39. What is the difference between ‘readonly’ and ‘const’?
‘const’ is a compile-time constant; ‘readonly’ is assigned at runtime, usually in the constructor.

### 40. What is boxing and unboxing?
Boxing converts a value type to an object type; unboxing extracts the value type from the object.

### 41. Explain async and await in C#.
They are used for asynchronous programming. ‘async’ marks a method as asynchronous, and ‘await’ pauses the method execution until the awaited task completes.

### 42. What is garbage collection in C#?
Garbage collection automatically frees memory occupied by objects that are no longer in use.

### 43. What are generics in C#?
Generics allow you to define classes, interfaces, and methods with a placeholder for the type of data they store or use.

### 44. What is a namespace in C#?
A namespace is a container for classes and other types, used to organize code and avoid naming conflicts.

---

### SOLID Principles in C#

#### 45. What are SOLID principles in C#?  
SOLID is an acronym representing five key object-oriented design principles to make software designs more understandable, flexible, and maintainable:
- **S**: Single Responsibility Principle – A class should have only one reason to change.
- **O**: Open/Closed Principle – Software entities should be open for extension but closed for modification.
- **L**: Liskov Substitution Principle – Subtypes must be substitutable for their base types.
- **I**: Interface Segregation Principle – No client should be forced to depend on methods it does not use.
- **D**: Dependency Inversion Principle – Depend on abstractions, not concretions.

---

### Common C# Design Patterns and Interview Questions

#### 46. What is the Singleton pattern?  
Ensures only one instance of a class exists and provides a global point of access.

**Example:**
```csharp
public sealed class Singleton {
    private static readonly Singleton instance = new Singleton();
    private Singleton() {}
    public static Singleton Instance => instance;
}
```

#### 47. What is the Factory pattern?  
Creates objects without specifying the exact class of object that will be created.

**Example:**
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

#### 48. What is the Repository pattern?  
Abstracts the data layer, providing a collection-like interface for accessing domain objects.

#### 49. What is the Observer pattern?  
Defines a one-to-many dependency so that when one object changes state, all its dependents are notified.

**Example:**  
Events/delegates in C# are commonly used for this.

#### 50. What is the Strategy pattern?  
Defines a family of algorithms, encapsulates each one, and makes them interchangeable.

#### 51. What is the Dependency Injection (DI) pattern?  
A technique where an object receives its dependencies from an external source rather than creating them itself. Widely used in ASP.NET Core with built-in DI container.

#### 52. What is the Adapter pattern?  
Allows incompatible interfaces to work together.

#### 53. What is the Decorator pattern?  
Adds new behaviors to objects dynamically by placing them inside special wrapper objects.

#### 54. What is the Command pattern?  
Encapsulates a request as an object, thereby allowing for parameterization and queuing of requests.

#### 55. What is the Mediator pattern?  
Defines an object that encapsulates how a set of objects interact, promoting loose coupling.

---

### C# 13 (2025) Latest Features

> As of 2025, C# 13 is the latest version. Below are the most notable features (based on official previews and proposals):

1. **Primary Constructors for All Types**  
   You can use primary constructors in any type (not just records), making it easier to declare and initialize fields.

   ```csharp
   public class Person(string name, int age) {
       public string Name { get; } = name;
       public int Age { get; } = age;
   }
   ```

2. **Collection Literals**  
   New syntax for easily creating collections.
   ```csharp
   var numbers = [1, 2, 3];
   var people = [new Person("A", 1), new Person("B", 2)];
   ```

3. **Parameter Null-Checking Simplification**  
   You can use the `!!` operator in parameter lists to auto-check for nulls.
   ```csharp
   void Save(string name!!) { ... }
   ```

4. **Lambda Expressions with Params**  
   Lambdas can now have `params` parameters.

5. **Better Pattern Matching Enhancements**  
   Improved `switch` expressions, list patterns, and property patterns.

6. **Extension Types (Preview)**  
   Attach static and extension members to existing types without modifying their source.

7. **Required Members for Structs**  
   You can now use `required` keyword for fields in structs, improving data integrity.

8. **Improved Interpolated String Handlers**  
   More efficient and flexible handling of interpolated strings, especially for logging and formatting.

9. **Experimental Features Toggle**  
   Ability to enable experimental language features in the project file.

10. **Other Minor Improvements**  
    - Better support for asynchronous streams.
    - Additional attributes for source generators and analyzers.
    - Improved error diagnostics and IDE tooling.

---

### .NET Threading, Tasks, Locks, and Synchronization - Deep Interview Questions

#### 56. What is a thread in .NET?  
A thread is the smallest unit of execution within a process. In .NET, threads are managed by the Thread class or via the Task Parallel Library.

#### 57. How do you create and start a thread in .NET?
```csharp
Thread t = new Thread(SomeMethod);
t.Start();
```

#### 58. What is the ThreadPool in .NET?  
The ThreadPool manages a pool of worker threads for short-lived operations, avoiding the overhead of manual thread management.

#### 59. What is a Task in .NET? How is it different from Thread?  
Task (System.Threading.Tasks.Task) represents an asynchronous operation and is part of TPL. Tasks are usually scheduled on the thread pool and can return values, support continuations, and handle exceptions more easily than raw threads.

#### 60. What is the difference between Task.Run and Task.Factory.StartNew?  
- Task.Run is a simplified API for Task.Factory.StartNew with default options for background work.
- Task.Factory.StartNew requires explicit configuration for scheduler, options, and state.

#### 61. What is a monitor in .NET?  
Monitor is a synchronization primitive that allows one thread at a time to execute a block of code (critical section). Used internally by the lock keyword.

#### 62. How does the lock keyword work?  
The lock statement ensures that only one thread can enter a critical section at a time. Internally, it uses Monitor.Enter and Monitor.Exit.

#### 63. What is deadlock? How can it happen in .NET?
A deadlock occurs when two or more threads are waiting for each other to release locks, causing all to be blocked indefinitely.

#### 64. What is a race condition?  
A race condition occurs when the outcome of a program depends on the sequence or timing of threads, typically due to unsynchronized access to shared data.

#### 65. How can you avoid deadlocks?
- Always acquire locks in a fixed global order.
- Use timeout for lock acquisition.
- Minimize lock scope.

#### 66. What is a Mutex? How is it different from lock/Monitor?  
A Mutex is used for inter-process synchronization (across processes), while lock and Monitor are for synchronization within a single process.

#### 67. What is a Semaphore and SemaphoreSlim?  
Semaphore allows a fixed number of threads to access a resource concurrently. SemaphoreSlim is a lightweight version for intra-process use.

#### 68. What is ReaderWriterLockSlim?  
ReaderWriterLockSlim allows multiple threads to read data but only one thread to write, increasing concurrency for read-heavy scenarios.

#### 69. What is Thread.Join()?  
Thread.Join() blocks the calling thread until the target thread completes.

#### 70. What is Thread.Abort()?  
Thread.Abort() requests the termination of a thread. It is obsolete and should be avoided due to ungraceful termination.

#### 71. What is Thread.Suspend() and Thread.Resume()?  
These methods are obsolete and dangerous due to potential for deadlocks and inconsistent state.

#### 72. How do you monitor the status of a Task?
You can use Task.Status property or await the Task for completion.

#### 73. What is Task.Wait() and Task.WaitAll()?  
- Task.Wait() blocks until the task completes.
- Task.WaitAll() blocks until all tasks complete.

#### 74. How do you cancel a Task?  
Use CancellationToken:
```csharp
CancellationTokenSource cts = new CancellationTokenSource();
Task t = Task.Run(() => { /* work */ }, cts.Token);
cts.Cancel(); // requests cancellation
```

#### 75. What is ConcurrentBag, ConcurrentDictionary, etc.?  
These are thread-safe collections in System.Collections.Concurrent namespace for multi-threaded scenarios.

#### 76. What is ThreadLocal<T>?  
ThreadLocal<T> provides thread-local storage, so each thread has its own value.

#### 77. Explain async/await in the context of threading.  
async/await does not create new threads but allows asynchronous, non-blocking code. The code after await resumes when the awaited task completes, possibly on a different thread.

#### 78. What are synchronization contexts?  
SynchronizationContext is an abstraction for scheduling work on different environments (UI thread, ASP.NET request, etc.). It controls how continuations after await run.

#### 79. What is Parallel.For and Parallel.ForEach?  
These are APIs in TPL for executing loop iterations in parallel, leveraging multiple threads from the thread pool.

#### 80. What is a Barrier?  
Barrier is a synchronization primitive for parallel algorithms, making threads wait until all reach a certain point.

#### 81. What is SpinLock and SpinWait?  
- SpinLock is a lock that repeatedly checks for lock availability (spins), useful when lock hold time is expected to be very short.
- SpinWait allows a thread to wait in a busy loop for a short time.

#### 82. What is a ManualResetEvent and AutoResetEvent?  
These are signaling primitives for thread synchronization. ManualResetEvent stays signaled until reset, while AutoResetEvent resets automatically after releasing a single thread.

#### 83. What is Volatile keyword?  
The volatile keyword tells the compiler not to cache the value of a field, ensuring that the latest value is always read from memory. Used for fields that are shared between threads.

#### 84. Explain Interlocked class usage.  
Interlocked provides atomic operations for variables shared between threads (e.g., Increment, Decrement, CompareExchange).

#### 85. Explain Thread.Sleep() and Thread.Yield().  
- Thread.Sleep pauses the current thread for a specified time.
- Thread.Yield signals the OS to switch to another thread but does not block.

#### 86. What is a background thread vs foreground thread?  
Foreground threads keep the process alive until they finish; background threads do not.

---

### Angular Exception Handling

#### 87. How does Angular handle exceptions?
Angular provides a global error handler using the `ErrorHandler` class. Uncaught errors in services, components, or RxJS streams are captured here.

#### 88. How do you implement custom global exception handling in Angular?
You can create a custom error handler by extending `ErrorHandler` and providing it in your app module.

#### 89. How can you handle HTTP errors in Angular?
Use RxJS `catchError` operator in services.

#### 90. How do you handle errors in Angular forms?
You can use validators and check for form control errors in the template to show error messages.

#### 91. How do you handle errors in Observables?
Use `catchError`, `retry`, `retryWhen` etc. in your RxJS pipeline.

---

### Angular Security Interview Questions

#### 92. What are common security risks in Angular applications?
Common risks include Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF), insecure direct object references, and improper authentication/authorization.

#### 93. How does Angular prevent XSS attacks?
Angular automatically escapes content in interpolations (`{{ ... }}`) and property bindings. Use `[innerHTML]` with care and consider using DomSanitizer for trusted values.

#### 94. What is DomSanitizer in Angular?
DomSanitizer is a service that helps prevent XSS by sanitizing potentially dangerous values before inserting them into the DOM.

#### 95. How can you secure API calls in Angular?
- Always use HTTPS
- Implement authentication (JWT, OAuth)
- Use HttpInterceptor to attach tokens and handle errors

#### 96. How to prevent CSRF in Angular?
Your backend should implement CSRF protection for session-based authentication. You can use HttpInterceptor to set CSRF tokens in requests.

#### 97. How do you handle authentication and authorization in Angular?
- Use route guards (`CanActivate`, `CanLoad`) for authorization
- Store tokens securely (prefer HttpOnly cookies)
- Use services to manage user authentication state

#### 98. What are best practices for handling sensitive data in Angular?
- Never store sensitive data in plain localStorage/sessionStorage
- Avoid exposing secrets in Angular source code (environment files)
- Always validate and sanitize data on the server side

#### 99. What is Content Security Policy (CSP) and how does it relate to Angular?
CSP is an HTTP header that helps prevent XSS attacks by restricting sources of content. Angular apps should be served with a strong CSP.

#### 100. How do you prevent open redirects in Angular routing?
Validate and sanitize redirect URLs. Avoid using dynamic values for navigation unless validated.

#### 101. How can you defend against clickjacking attacks in Angular?
Set appropriate headers (`X-Frame-Options`, `Content-Security-Policy: frame-ancestors`) on the server to prevent your app from being loaded in an iframe.

---

*Keep updating this file to make your preparation easier!*
