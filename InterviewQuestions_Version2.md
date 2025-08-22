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

## C# Interview Questions

### 16. What is C#?
C# is a modern, object-oriented programming language developed by Microsoft for the .NET platform.

### 17. What are value types and reference types in C#?
Value types store data directly (e.g., int, struct), while reference types store references to data (e.g., class, interface).

### 18. Explain the difference between an interface and an abstract class.
An abstract class can provide method implementations and fields, while an interface only declares methods and properties (since C# 8.0, interfaces can have default implementations).

### 19. What is the difference between ‘==’ and ‘Equals()’ in C#?
‘==’ is an operator that can be overloaded for value or reference equality, while ‘Equals()’ is a method that checks for value equality.

### 20. What is LINQ?
Language Integrated Query (LINQ) is a feature for querying data from different sources using C# syntax.

### 21. What are delegates in C#?
Delegates are type-safe function pointers used to encapsulate methods and support events and callbacks.

### 22. What is an event in C#?
An event is a message sent by an object to signal the occurrence of an action. Events use delegates under the hood.

### 23. What is exception handling in C#?
Exception handling uses try, catch, finally, and throw keywords to handle runtime errors gracefully.

### 24. What is the difference between ‘readonly’ and ‘const’?
‘const’ is a compile-time constant; ‘readonly’ is assigned at runtime, usually in the constructor.

### 25. What is boxing and unboxing?
Boxing converts a value type to an object type; unboxing extracts the value type from the object.

### 26. Explain async and await in C#.
They are used for asynchronous programming. ‘async’ marks a method as asynchronous, and ‘await’ pauses the method execution until the awaited task completes.

### 27. What is garbage collection in C#?
Garbage collection automatically frees memory occupied by objects that are no longer in use.

### 28. What are generics in C#?
Generics allow you to define classes, interfaces, and methods with a placeholder for the type of data they store or use.

### 29. What is a namespace in C#?
A namespace is a container for classes and other types, used to organize code and avoid naming conflicts.

---

*Keep updating this file to make your preparation easier!*