# Architecture Rules & Best Practices

## Modular Monolith Boundaries
- **Domain Isolation**: Code must be organized by domain modules, not technical layers. Keep domains cohesive.
- **Strict Contracts**: Do not import internal functions from one domain module directly into another. Always use designated public interfaces, DTOs, or facades.
- **Security**: Never store secrets in plain text. Always use Environment variables (`.env`) via Laravel's `config()` helpers.

## Native-First & Simplicity Mandate (KISS)
- **Framework Over Custom**: Evaluate Laravel 12, PHP 8.4, and Vue 3/Inertia native solutions before writing custom logic.
- **Laravel Helpers**: Strictly use built-in tools (Collections, `Str::`, `Arr::`, native validation, Eloquent scopes) instead of manual loops or array manipulation.
- **PHP 8.4 Features**: Use constructor promotion, match expressions, readonly classes, property hooks, and arrow functions to minimize boilerplate.
- **No Over-Engineering**: Write the simplest code to pass the tests. Do not build abstract factories, repositories, or complex design patterns unless explicitly requested.

## Laravel 12 Best Practices
- **Routing & Controllers**: Keep controllers thin. Use FormRequests for validation and authorization. Move heavy business logic to Action classes or Jobs.
- **Eloquent ORM**: Strictly type Eloquent models. Prefer Eloquent scopes and relationships over raw SQL queries. Always prevent N+1 queries by eager loading (`with()`).
- **Dependency Injection**: Leverage Laravel's Service Container. Inject dependencies into constructors or methods instead of using the `new` keyword.
- **Background Jobs**: Use Laravel Queues (e.g., Horizon) for slow or third-party operations. Return responses to the user immediately.
- **Events & Listeners**: Use Laravel's event system to decouple cross-module side-effects.

## Vue 3 & Inertia.js Best Practices
- **Composition API**: Exclusively use `<script setup>` and the Composition API (`ref`, `computed`, `watch`). Do NOT use the Options API.
- **Reactivity**: Prefer `ref()` over `reactive()` for consistency. Avoid deeply nested reactivity where possible.
- **Inertia.js**: Use Inertia's `<Link>` and `useForm()` helpers for navigation and state management. Avoid manual `axios` or `fetch` calls for standard page navigation or form submissions.
- **Components**: Write Single File Components (SFCs). Keep them small, single-purpose, and modular.
- **State Management**: Prefer local component state and VueUse composables. Avoid global state managers (like Pinia) unless shared global state is absolutely unavoidable.
- **Styling**: Use Tailwind CSS utility classes. Avoid writing custom CSS/SCSS unless explicitly required for complex animations or overrides.