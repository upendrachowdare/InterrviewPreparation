# Angular Interview Questions

## Table of Contents
- [What is Angular?](#what-is-angular)
- [What are Angular components?](#what-are-angular-components)
- [Angular Standalone APIs](#angular-standalone-apis)
- [Angular Signals](#angular-signals)
- [Angular Change Detection](#angular-change-detection)
- [Angular Dependency Injection](#angular-dependency-injection)
- [RxJS in Angular](#rxjs-in-angular)
- [Top 10 RxJS Operators](#top-10-rxjs-operators)
- [Angular Routing](#angular-routing)
- [Angular Lifecycle Hooks](#angular-lifecycle-hooks)
- [Performance Optimization](#performance-optimization)
- [Testing in Angular](#testing-in-angular)
- [Best Practices](#best-practices)
- [Angular 20 New Features](#angular-20-new-features)

---

### What is Angular?
Angular is a TypeScript-based framework for building scalable web applications, maintained by Google.

### What are Angular components?
Components are the base UI building blocks in Angular, defined by a TypeScript class, HTML template, and styles.

### Angular Standalone APIs
Standalone APIs allow building Angular apps without NgModules, making the structure simpler and modular.

### Angular Signals
Signals are a reactivity primitive that lets you track and update values and automatically update the UI when the value changes.

### Angular Change Detection
Angular uses zone.js and a change detection tree to track and update the DOM. Signals and OnPush strategy can optimize performance.

### Angular Dependency Injection
Angular DI is a hierarchical injector system that provides dependencies to classes/components at runtime.

### RxJS in Angular
RxJS is used for reactive programming, handling async data streams like HTTP, user input, etc.

### Top 10 RxJS Operators
- map
- filter
- switchMap
- mergeMap
- debounceTime
- take
- takeUntil
- combineLatest
- catchError
- distinctUntilChanged

### Angular Routing
Angular Router enables SPA navigation and lazy loading of modules.

### Angular Lifecycle Hooks
- ngOnInit
- ngOnDestroy
- ngOnChanges
- ngAfterViewInit
- ngAfterContentInit
- ngDoCheck

### Performance Optimization
- Use OnPush Change Detection
- TrackBy with ngFor
- Lazy load routes/modules
- Avoid memory leaks with takeUntil
- Preload strategies

### Testing in Angular
- Jasmine for unit testing
- TestBed for component tests
- HttpTestingController for HTTP tests

### Best Practices
- Use SCAM (Single Component Angular Module) when using modules
- Prefer Standalone APIs for new projects
- Use strict typing everywhere
- Use environment variables

### Angular 20 New Features
- Standalone APIs (default)
- Signal-based components
- New control flow (@for, @if)
- Improved SSR/hydration
- Deferred loading with @defer
- Smaller bundles, faster builds

---

[Back to Top](#table-of-contents)