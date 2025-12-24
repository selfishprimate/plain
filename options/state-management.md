# State Management

State management is the practice of managing and synchronizing data (state) across your application components. As applications grow, sharing data between components, handling user interactions, and keeping the UI in sync with data becomes complex. State management solutions provide patterns and tools to handle this complexity in a predictable, maintainable way.

## What is State Management?

State refers to any data that can change over time in your application - user information, form inputs, UI toggles, fetched data, etc. State management involves:

- **Storing** application data in a centralized or distributed manner
- **Updating** state in response to user actions or events
- **Synchronizing** UI components with state changes
- **Sharing** state between components efficiently
- **Persisting** state across sessions when needed

### When Do You Need State Management?

Simple applications with minimal component communication may not need dedicated state management - component state and props are sufficient. However, you need state management when:

- Multiple components need to access the same data
- Components need to communicate across different parts of the component tree
- State needs to persist across route changes
- You're experiencing "prop drilling" (passing props through many levels)
- Application state is becoming difficult to track and debug
- You need time-travel debugging or state history
- Multiple data sources need to be synchronized

## React State Management

React's ecosystem offers the most diverse state management solutions, from simple to complex, catering to different application needs and philosophies.

### Redux Toolkit (RTK)
The official, opinionated, batteries-included toolset for Redux.
- **Best for:** Large applications, complex state logic, teams needing structure
- **Philosophy:** Predictable state container with unidirectional data flow
- **Key Features:**
  - DevTools with time-travel debugging
  - RTK Query for data fetching
  - Immer for immutable updates
  - Built-in middleware
  - TypeScript support
- **When to use:**
  - Large-scale applications with complex state
  - Need predictable state updates
  - Want excellent debugging tools
  - Team prefers explicit over implicit
  - Need middleware for side effects
  - Want established patterns and best practices
- **Learning curve:** Medium (simpler than classic Redux)
- **Bundle size:** ~12kb (RTK) + ~2kb (React-Redux)
- **Performance:** Excellent with proper memoization
- **Community:** Massive, most popular solution

### Zustand
A small, fast, and scalable state management solution.
- **Best for:** Modern React apps, rapid development, small to medium projects
- **Philosophy:** Simplified state management without boilerplate
- **Key Features:**
  - No providers needed
  - TypeScript ready
  - Async actions support
  - Middleware system
  - DevTools support
  - Subscribe to state slices
- **When to use:**
  - Want minimal boilerplate
  - Building small to medium apps
  - Need simple but powerful solution
  - Like hooks-based API
  - Want small bundle size
  - Need quick setup
- **Learning curve:** Low
- **Bundle size:** ~3kb
- **Performance:** Excellent, automatic optimization
- **Community:** Rapidly growing, modern

### MobX
Reactive state management with automatic tracking.
- **Best for:** Complex applications with lots of derived state
- **Philosophy:** Anything that can be derived from state, should be derived automatically
- **Key Features:**
  - Automatic dependency tracking
  - Computed values
  - Reactions and autorun
  - Class or object-based
  - Multiple stores
  - TypeScript support
- **When to use:**
  - Have complex derived state
  - Prefer OOP patterns
  - Want automatic reactivity
  - Building data-heavy applications
  - Like minimal boilerplate
  - Need fine-grained reactivity
- **Learning curve:** Medium-High
- **Bundle size:** ~15kb
- **Performance:** Excellent with automatic optimization
- **Community:** Large, established

### Recoil
Facebook's experimental state management library.
- **Best for:** Complex React apps needing fine-grained subscriptions
- **Philosophy:** Atom-based state with React Suspense integration
- **Key Features:**
  - Atoms and selectors
  - React Suspense support
  - Async selectors
  - Time-travel debugging
  - Fine-grained subscriptions
  - Graph-based state
- **When to use:**
  - Need React Suspense integration
  - Want graph-based state dependencies
  - Building Facebook-scale apps
  - Need fine-grained reactivity
  - Want derived state management
- **Learning curve:** Medium-High
- **Bundle size:** ~30kb
- **Status:** Still experimental
- **Community:** Growing, Facebook-backed

### Jotai
Primitive and flexible state management for React.
- **Best for:** Modern React apps, atomic state management
- **Philosophy:** Atomic approach to state management
- **Key Features:**
  - Atom-based like Recoil
  - No providers needed
  - React Suspense support
  - Async support built-in
  - TypeScript first
  - DevTools support
- **When to use:**
  - Want Recoil-like atoms but simpler
  - Building with React Suspense
  - Need flexible atomic state
  - Want minimal API
  - Like bottom-up state
- **Learning curve:** Low-Medium
- **Bundle size:** ~3kb
- **Performance:** Excellent
- **Community:** Growing, modern

### Valtio
Proxy-based state management for React.
- **Best for:** Simple state management with mutable API
- **Philosophy:** Make proxy-state simple
- **Key Features:**
  - Mutable state with proxies
  - Snapshot for immutability
  - Subscribe to changes
  - DevTools support
  - TypeScript support
  - Works outside React
- **When to use:**
  - Want mutable state API
  - Like simple mental model
  - Need state outside React
  - Building simple to medium apps
  - Want minimal boilerplate
- **Learning curve:** Low
- **Bundle size:** ~3kb
- **Performance:** Good
- **Community:** Growing

### Context API + useReducer
React's built-in state management solution.
- **Best for:** Small apps, avoiding external dependencies
- **Philosophy:** Built-in React patterns
- **Key Features:**
  - No external dependencies
  - Native React patterns
  - Works with React DevTools
  - TypeScript support
- **When to use:**
  - Small applications
  - Want to avoid dependencies
  - Simple state requirements
  - Learning React patterns
  - Building libraries
- **Learning curve:** Low
- **Bundle size:** 0kb (built-in)
- **Performance:** Can cause unnecessary re-renders
- **Limitations:** No DevTools, performance concerns

### TanStack Query (React Query)
Powerful asynchronous state management for server state.
- **Best for:** Server state, data fetching, caching
- **Philosophy:** Server state is different from client state
- **Key Features:**
  - Caching and synchronization
  - Background refetching
  - Optimistic updates
  - Pagination support
  - Infinite queries
  - Mutations
- **When to use:**
  - Managing server state
  - Need caching strategy
  - Want background updates
  - Building data-heavy apps
  - Need optimistic UI
- **Learning curve:** Medium
- **Bundle size:** ~13kb
- **Performance:** Excellent caching
- **Community:** Large, active

### XState
JavaScript state machines and statecharts.
- **Best for:** Complex UI flows, multi-step forms, games
- **Philosophy:** Finite state machines for predictable logic
- **Key Features:**
  - Visual statechart editor
  - Hierarchical states
  - Parallel states
  - History states
  - Actions and guards
  - TypeScript support
- **When to use:**
  - Complex UI workflows
  - Multi-step processes
  - Need visual representation
  - Want predictable state transitions
  - Building games or animations
- **Learning curve:** High
- **Bundle size:** ~15kb
- **Performance:** Excellent
- **Community:** Growing, unique approach

### Legend State
Superfast observable-based state management.
- **Best for:** Performance-critical apps, large datasets
- **Philosophy:** Fastest possible reactivity
- **Key Features:**
  - Blazing fast performance
  - Fine-grained reactivity
  - Persistence plugins
  - React and React Native
  - TypeScript support
- **When to use:**
  - Performance is critical
  - Large amounts of state
  - React Native apps
  - Need persistence
- **Learning curve:** Low-Medium
- **Bundle size:** ~4kb
- **Performance:** Best in class
- **Community:** Small but growing

### Rematch
Redux made simple.
- **Best for:** Teams wanting Redux patterns without boilerplate
- **Philosophy:** Redux best practices without the boilerplate
- **Key Features:**
  - Redux DevTools
  - Plugin system
  - TypeScript support
  - Async/await support
  - Multiple models
- **When to use:**
  - Like Redux patterns
  - Want less boilerplate
  - Need plugins
  - Team knows Redux
- **Learning curve:** Low-Medium
- **Bundle size:** ~7kb
- **Performance:** Good
- **Community:** Moderate

## Vue State Management

Vue's ecosystem provides elegant solutions that integrate seamlessly with Vue's reactivity system.

### Pinia
The official state management library for Vue (replacing Vuex).
- **Best for:** All Vue 3 applications needing state management
- **Philosophy:** Intuitive, type-safe, extensible
- **Key Features:**
  - DevTools support
  - Hot module replacement
  - TypeScript support
  - Plugins system
  - No mutations
  - Composition API support
- **When to use:**
  - Any Vue 3 app needing state
  - Want official solution
  - Need DevTools
  - Like simple API
  - Building with Nuxt 3
- **Learning curve:** Low
- **Bundle size:** ~2kb
- **Performance:** Excellent
- **Community:** Official, growing rapidly

### Vuex
The previous official state management for Vue.
- **Best for:** Vue 2 apps, legacy projects
- **Philosophy:** Flux-inspired pattern for Vue
- **Key Features:**
  - Mutations and actions
  - Modules system
  - DevTools support
  - Time-travel debugging
  - Plugins
- **When to use:**
  - Vue 2 applications
  - Legacy projects
  - Team familiar with Vuex
  - Need strict patterns
- **Learning curve:** Medium
- **Bundle size:** ~10kb
- **Performance:** Good
- **Status:** Maintenance mode, use Pinia for new projects

### Harlem
Simple, unopinionated state management for Vue 3.
- **Best for:** Vue 3 apps wanting simplicity
- **Philosophy:** Minimalist approach
- **Key Features:**
  - Simple API
  - DevTools support
  - Plugin architecture
  - TypeScript support
  - Lazy loading stores
- **When to use:**
  - Want minimal API
  - Building small to medium apps
  - Like unopinionated tools
- **Learning curve:** Low
- **Bundle size:** ~2kb
- **Community:** Small

## Angular State Management

Angular applications typically use RxJS-based solutions that complement Angular's reactive architecture.

### NgRx
Reactive state management for Angular based on Redux.
- **Best for:** Large Angular apps, enterprise applications
- **Philosophy:** Redux pattern with RxJS
- **Key Features:**
  - Redux DevTools
  - Effects for side effects
  - Entity management
  - Router state
  - Schematics
  - Strong typing
- **When to use:**
  - Large Angular applications
  - Enterprise requirements
  - Need predictable state
  - Want debugging tools
  - Team likes Redux
- **Learning curve:** High
- **Bundle size:** ~20kb
- **Performance:** Good with OnPush
- **Community:** Official recommendation

### Akita
Simple and effective state management for Angular.
- **Best for:** Angular apps wanting simpler alternative to NgRx
- **Philosophy:** Object-oriented, less boilerplate
- **Key Features:**
  - Entity stores
  - DevTools
  - Query library
  - Plugins system
  - Server-side rendering
- **When to use:**
  - Want simpler than NgRx
  - Like OOP patterns
  - Building CRUD apps
  - Need entity management
- **Learning curve:** Medium
- **Bundle size:** ~15kb
- **Performance:** Good
- **Community:** Moderate

### Elf
Reactive immutable state management for Angular.
- **Best for:** Modern Angular apps
- **Philosophy:** Functional reactive programming
- **Key Features:**
  - Immutable state
  - DevTools
  - Persistence
  - Entities support
  - Requests tracking
- **When to use:**
  - Want modern approach
  - Like functional programming
  - Need immutability
  - Building modern Angular apps
- **Learning curve:** Medium
- **Bundle size:** ~5kb
- **Performance:** Excellent
- **Community:** Growing

### NGXS
State management pattern + library for Angular.
- **Best for:** Angular apps wanting decorators-based approach
- **Philosophy:** Less boilerplate with decorators
- **Key Features:**
  - Decorators-based
  - DevTools
  - Plugins ecosystem
  - Snapshot selects
  - Action handlers
- **When to use:**
  - Like decorators
  - Want less boilerplate than NgRx
  - Building medium to large apps
  - Need plugins
- **Learning curve:** Medium
- **Bundle size:** ~20kb
- **Performance:** Good
- **Community:** Active

### RxAngular State
Reactive state management with RxJS.
- **Best for:** RxJS-heavy Angular apps
- **Philosophy:** Fully reactive with RxJS
- **Key Features:**
  - Local component state
  - Global state
  - Fully reactive
  - TypeScript support
- **When to use:**
  - Heavy RxJS usage
  - Want full reactivity
  - Like streaming approach
- **Learning curve:** High (need RxJS knowledge)
- **Bundle size:** ~10kb
- **Performance:** Excellent
- **Community:** Small

## Svelte State Management

Svelte's built-in reactivity reduces the need for external state management, but options exist for complex apps.

### Svelte Stores
Built-in reactive store system.
- **Best for:** Most Svelte applications
- **Philosophy:** Simple, reactive stores
- **Key Features:**
  - Writable stores
  - Readable stores
  - Derived stores
  - Custom stores
  - Auto-subscription
- **When to use:**
  - Any Svelte app
  - Start here first
  - Simple to medium complexity
  - Want built-in solution
- **Learning curve:** Low
- **Bundle size:** 0kb (built-in)
- **Performance:** Excellent
- **Community:** Core feature

### Svelte Store Plus
Enhanced stores with additional features.
- **Best for:** Apps needing more than basic stores
- **Philosophy:** Extend native stores
- **Key Features:**
  - Async stores
  - Storage sync
  - History tracking
  - Computed stores
- **When to use:**
  - Need enhanced stores
  - Want async handling
  - Need persistence
- **Learning curve:** Low
- **Bundle size:** ~2kb
- **Community:** Small

## Solid State Management

SolidJS's fine-grained reactivity makes state management simpler with built-in primitives.

### Solid Stores
Built-in nested reactivity system.
- **Best for:** Most Solid applications
- **Philosophy:** Fine-grained reactive stores
- **Key Features:**
  - Nested reactivity
  - Path-based updates
  - Immutable updates
  - Reconciliation
- **When to use:**
  - Any Solid app
  - Need nested state
  - Want built-in solution
- **Learning curve:** Low-Medium
- **Bundle size:** 0kb (built-in)
- **Performance:** Excellent
- **Community:** Core feature

## Cross-Framework Solutions

State management solutions that work across different frameworks or vanilla JavaScript.

### Nano Stores
Tiny state manager for React, Vue, Svelte, and vanilla.
- **Best for:** Multi-framework projects, micro-frontends
- **Philosophy:** Framework agnostic atoms
- **Key Features:**
  - 300 bytes core
  - Framework adapters
  - TypeScript support
  - Computed stores
  - Tasks (async)
- **When to use:**
  - Multiple frameworks
  - Micro-frontends
  - Want tiny size
  - Need portability
- **Learning curve:** Low
- **Bundle size:** <1kb
- **Performance:** Excellent
- **Community:** Growing

### Effector
Multi-platform state manager.
- **Best for:** Complex applications, any framework
- **Philosophy:** Event-driven, declarative
- **Key Features:**
  - Events, stores, effects
  - Combine stores
  - TypeScript support
  - DevTools
  - SSR support
- **When to use:**
  - Complex business logic
  - Multiple platforms
  - Want predictability
  - Like event-driven
- **Learning curve:** Medium-High
- **Bundle size:** ~10kb
- **Performance:** Excellent
- **Community:** Active

### Storeon
Tiny event-based state manager.
- **Best for:** Small apps, any framework
- **Philosophy:** Event-driven Redux-like
- **Key Features:**
  - 180 bytes core
  - Modular
  - TypeScript support
  - DevTools
  - Framework adapters
- **When to use:**
  - Want tiny size
  - Simple state needs
  - Like Redux pattern
  - Multiple frameworks
- **Learning curve:** Low
- **Bundle size:** <1kb
- **Performance:** Good
- **Community:** Small

## Specialized Solutions

State management for specific use cases.

### Hookstate
State management for React with DevTools.
- **Best for:** React apps wanting simple but powerful state
- **Philosophy:** Direct state mutations with proxies
- **Key Features:**
  - Local and global state
  - DevTools
  - Plugins
  - Validation
  - Persistence
- **When to use:**
  - Want direct mutations
  - Need DevTools
  - Like simple API
- **Learning curve:** Low
- **Bundle size:** ~5kb
- **Community:** Moderate

### Overmind
Frictionless state management.
- **Best for:** Apps wanting explicit state management
- **Philosophy:** Explicit, simple, powerful
- **Key Features:**
  - DevTools with time-travel
  - TypeScript support
  - Effects management
  - Derived state
- **When to use:**
  - Want explicit patterns
  - Need great DevTools
  - Like clear separation
- **Learning curve:** Medium
- **Bundle size:** ~15kb
- **Community:** Stable

### Easy Peasy
Vegetarian-friendly Redux.
- **Best for:** Redux-like experience without boilerplate
- **Philosophy:** Redux made easy
- **Key Features:**
  - Redux DevTools
  - Thunks built-in
  - Computed values
  - TypeScript support
  - Listeners
- **When to use:**
  - Like Redux concepts
  - Want less boilerplate
  - Need computed values
- **Learning curve:** Low-Medium
- **Bundle size:** ~15kb
- **Community:** Moderate

## Form State Management

Specialized solutions for managing form state.

### React Hook Form
Performant forms with minimal re-renders.
- **Best for:** React forms
- **Features:** Validation, minimal re-renders, tiny size
- **Bundle size:** ~25kb
- **Learning curve:** Low-Medium

### Formik
Popular form library for React.
- **Best for:** Complex React forms
- **Features:** Validation, field arrays, nested objects
- **Bundle size:** ~15kb
- **Learning curve:** Medium

### React Final Form
High performance form state management.
- **Best for:** Complex form requirements
- **Features:** Field-level validation, pristine/dirty tracking
- **Bundle size:** ~8kb
- **Learning curve:** Medium

### VeeValidate
Form validation for Vue.
- **Best for:** Vue forms
- **Features:** Validation rules, composition API
- **Bundle size:** ~25kb
- **Learning curve:** Low-Medium

## Selection Criteria

Consider these factors when choosing state management:

- **Application Size:** Simple apps may only need component state
- **Team Experience:** Choose familiar patterns when possible
- **Performance Needs:** Consider re-render optimization
- **DevTools Requirements:** Debugging and time-travel needs
- **TypeScript Support:** Type safety requirements
- **Bundle Size:** Performance budget constraints
- **Learning Curve:** Team onboarding time
- **Community Support:** Documentation and help availability
- **Framework Alignment:** Native vs external solutions
- **Specific Features:** SSR, persistence, middleware needs

### General Recommendations

- **Start Simple:** Use component state first, add state management when needed
- **React:** Zustand for simplicity, Redux Toolkit for large apps, TanStack Query for server state
- **Vue:** Pinia for all new Vue 3 apps
- **Angular:** NgRx for large apps, Akita for simpler needs
- **Svelte:** Built-in stores for most cases
- **Solid:** Built-in stores with fine-grained reactivity

---

*State management is about finding the right balance between simplicity and capability. Start with the simplest solution that meets your needs, and migrate to more complex solutions only when necessary. The best state management is the one your team understands and can maintain effectively.*