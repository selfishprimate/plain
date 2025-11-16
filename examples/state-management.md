# State Management: Options & Examples

This guide helps you choose the right state management solution for your frontend application.

---

## What is State Management?

State management is how your app tracks and updates data across components. This includes:
- User authentication status
- Form inputs
- API data
- UI state (modals, sidebars, themes)
- Shopping cart contents
- User preferences

**Key Questions:**
- Where does state live? (component, global, server)
- How is state updated? (actions, setters, mutations)
- How do components access state? (props, context, subscriptions)

---

## Option 1: React useState (Local State)

**Best for:** Simple apps, component-specific state

**Description:**
Built-in React hook for managing state within a single component.

**Pros:**
- Built into React (no dependencies)
- Simple to understand
- Perfect for local UI state
- No boilerplate

**Cons:**
- Doesn't scale well
- Prop drilling for shared state
- No dev tools
- Difficult to share across components

**Best Use Cases:**
- Form inputs
- Toggle states (show/hide)
- Component-specific UI state

**Example:**
```jsx
import { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
}
```

**When to Use:**
- State is only used in one component
- Simple UI state (modals, dropdowns)
- No need to share data

---

## Option 2: React Context (Shared State)

**Best for:** Theme, auth, simple global state

**Description:**
React's built-in way to share state across components without prop drilling.

**Pros:**
- Built into React
- No external dependencies
- Good for simple shared state
- Avoid prop drilling

**Cons:**
- Re-renders all consumers when state changes
- Can get messy with complex state
- No dev tools
- Requires boilerplate

**Best Use Cases:**
- Theme (light/dark mode)
- Authentication state
- User preferences
- Simple global settings

**Example:**
```jsx
import { createContext, useContext, useState } from 'react';

const ThemeContext = createContext();

export function ThemeProvider({ children }) {
  const [theme, setTheme] = useState('light');

  return (
    <ThemeContext.Provider value={{ theme, setTheme }}>
      {children}
    </ThemeContext.Provider>
  );
}

export function useTheme() {
  return useContext(ThemeContext);
}

// Usage
function App() {
  const { theme, setTheme } = useTheme();
  return <button onClick={() => setTheme('dark')}>Dark Mode</button>;
}
```

**When to Use:**
- 2-3 pieces of global state
- Theme or auth
- Not frequently updated

---

## Option 3: Zustand (Simple Global State)

**Best for:** Modern apps, simple API, minimal boilerplate

**Description:**
Lightweight state management with a hook-based API. Like Redux but simpler.

**Pros:**
- Tiny bundle size (~1KB)
- Simple, intuitive API
- No boilerplate
- Dev tools available
- Great TypeScript support
- Selective re-renders

**Cons:**
- Less mature than Redux
- Smaller ecosystem
- No time-travel debugging

**Best Use Cases:**
- Modern React apps
- Global state without complexity
- When Redux feels too heavy

**Installation:**
```bash
npm install zustand
```

**Example:**
```jsx
import create from 'zustand';

const useStore = create((set) => ({
  count: 0,
  user: null,
  increment: () => set((state) => ({ count: state.count + 1 })),
  setUser: (user) => set({ user }),
}));

// Usage
function Counter() {
  const { count, increment } = useStore();
  return <button onClick={increment}>{count}</button>;
}

function UserProfile() {
  const user = useStore((state) => state.user); // Only subscribes to user
  return <div>{user?.name}</div>;
}
```

**When to Use:**
- You need global state but Redux is overkill
- Want simple, modern state management
- TypeScript projects

**Learn More:** https://zustand-demo.pmnd.rs

---

## Option 4: Redux Toolkit (Complex Global State)

**Best for:** Large apps, complex state, time-travel debugging

**Description:**
The official, recommended way to use Redux. Simplifies Redux setup and reduces boilerplate.

**Pros:**
- Industry standard
- Excellent dev tools
- Time-travel debugging
- Mature ecosystem
- Great for complex state
- Strong TypeScript support

**Cons:**
- Steeper learning curve
- More boilerplate than Zustand
- Larger bundle size
- Can be overkill for small apps

**Best Use Cases:**
- Large, complex applications
- Teams familiar with Redux
- Apps with complex state logic
- Time-travel debugging needed

**Installation:**
```bash
npm install @reduxjs/toolkit react-redux
```

**Example:**
```jsx
import { configureStore, createSlice } from '@reduxjs/toolkit';
import { Provider, useSelector, useDispatch } from 'react-redux';

const counterSlice = createSlice({
  name: 'counter',
  initialState: { value: 0 },
  reducers: {
    increment: (state) => {
      state.value += 1; // Immer allows "mutating" code
    },
  },
});

const store = configureStore({
  reducer: {
    counter: counterSlice.reducer,
  },
});

// Usage
function App() {
  return (
    <Provider store={store}>
      <Counter />
    </Provider>
  );
}

function Counter() {
  const count = useSelector((state) => state.counter.value);
  const dispatch = useDispatch();

  return (
    <button onClick={() => dispatch(counterSlice.actions.increment())}>
      {count}
    </button>
  );
}
```

**When to Use:**
- Large applications
- Complex state logic
- Need Redux ecosystem
- Team already knows Redux

**Learn More:** https://redux-toolkit.js.org

---

## Option 5: React Query / TanStack Query (Server State)

**Best for:** API data, caching, background sync

**Description:**
Not traditional state management—it's designed specifically for server state (data from APIs).

**Pros:**
- Perfect for API data
- Auto caching and refetching
- Background updates
- Pagination and infinite scroll
- Optimistic updates
- Minimal boilerplate

**Cons:**
- Only for server state (not local UI state)
- Learning curve
- Requires backend API

**Best Use Cases:**
- Fetching and caching API data
- Real-time data sync
- Paginated lists
- Infinite scroll

**Installation:**
```bash
npm install @tanstack/react-query
```

**Example:**
```jsx
import { useQuery, useMutation, QueryClient, QueryClientProvider } from '@tanstack/react-query';

const queryClient = new QueryClient();

function App() {
  return (
    <QueryClientProvider client={queryClient}>
      <Todos />
    </QueryClientProvider>
  );
}

function Todos() {
  const { data, isLoading } = useQuery({
    queryKey: ['todos'],
    queryFn: () => fetch('/api/todos').then((res) => res.json()),
  });

  const mutation = useMutation({
    mutationFn: (newTodo) => fetch('/api/todos', {
      method: 'POST',
      body: JSON.stringify(newTodo),
    }),
    onSuccess: () => {
      queryClient.invalidateQueries({ queryKey: ['todos'] });
    },
  });

  if (isLoading) return 'Loading...';

  return (
    <div>
      {data.map((todo) => (
        <div key={todo.id}>{todo.title}</div>
      ))}
      <button onClick={() => mutation.mutate({ title: 'New Todo' })}>
        Add Todo
      </button>
    </div>
  );
}
```

**When to Use:**
- App relies heavily on API data
- Want smart caching and refetching
- Background sync needed

**Learn More:** https://tanstack.com/query

---

## Option 6: Jotai (Atomic State)

**Best for:** Atomic, bottom-up state

**Description:**
Primitive and flexible state management with an atomic approach.

**Pros:**
- Simple API
- TypeScript-first
- Bottom-up approach (compose atoms)
- No boilerplate
- Tiny bundle size

**Cons:**
- Less common
- Smaller ecosystem
- Learning curve for atomic pattern

**Installation:**
```bash
npm install jotai
```

**Example:**
```jsx
import { atom, useAtom } from 'jotai';

const countAtom = atom(0);

function Counter() {
  const [count, setCount] = useAtom(countAtom);
  return <button onClick={() => setCount((c) => c + 1)}>{count}</button>;
}
```

**When to Use:**
- Want atomic state pattern
- TypeScript projects
- Composable state

**Learn More:** https://jotai.org

---

## Option 7: Recoil (Atomic State by Meta)

**Best for:** Complex derived state, atomic patterns

**Description:**
Created by Meta (Facebook). Similar to Jotai but more features.

**Pros:**
- Atomic state model
- Derived state (selectors)
- Time-travel debugging
- Backed by Meta

**Cons:**
- Still experimental
- Larger than Zustand/Jotai
- Less adoption than Redux

**Installation:**
```bash
npm install recoil
```

**Example:**
```jsx
import { atom, selector, useRecoilState, useRecoilValue } from 'recoil';

const countState = atom({
  key: 'countState',
  default: 0,
});

const doubleCountState = selector({
  key: 'doubleCountState',
  get: ({ get }) => {
    const count = get(countState);
    return count * 2;
  },
});

function Counter() {
  const [count, setCount] = useRecoilState(countState);
  const doubleCount = useRecoilValue(doubleCountState);

  return (
    <>
      <button onClick={() => setCount((c) => c + 1)}>{count}</button>
      <div>Double: {doubleCount}</div>
    </>
  );
}
```

**When to Use:**
- Complex derived state
- Want atomic model
- Backed by Meta (trust factor)

**Learn More:** https://recoiljs.org

---

## Decision Guide

| **Your Need** | **Recommended Solution** |
|---|---|
| Local component state | React useState |
| Theme, auth (simple global) | React Context |
| Modern global state | Zustand |
| Large app, complex state | Redux Toolkit |
| API data, caching | React Query (TanStack Query) |
| Atomic state, TypeScript | Jotai |
| Derived state, selectors | Recoil |

---

## Comparison Table

| **Library** | **Bundle Size** | **Learning Curve** | **Best For** |
|---|---|---|---|
| useState | Built-in | Easy | Local state |
| Context | Built-in | Easy | Simple global |
| Zustand | ~1KB | Easy | Modern global state |
| Redux Toolkit | ~15KB | Medium | Large apps |
| React Query | ~12KB | Medium | Server state |
| Jotai | ~3KB | Medium | Atomic state |
| Recoil | ~20KB | Medium | Complex derived state |

---

## Combining Solutions

**Common Pattern:**
- **Zustand** for global UI state (theme, user)
- **React Query** for server data (API calls)
- **useState** for local component state

**Example Stack:**
```jsx
// Global state
import create from 'zustand';
const useStore = create((set) => ({
  theme: 'light',
  setTheme: (theme) => set({ theme }),
}));

// Server state
import { useQuery } from '@tanstack/react-query';
const { data } = useQuery(['todos'], fetchTodos);

// Local state
const [isOpen, setIsOpen] = useState(false);
```

---

## State Management Checklist

- [ ] Identify types of state (local, global, server)
- [ ] Choose solution for each type
- [ ] Set up dev tools
- [ ] Document state structure
- [ ] Plan for persistence (localStorage)
- [ ] Consider TypeScript types

---

## Resources

- **Zustand:** https://zustand-demo.pmnd.rs
- **Redux Toolkit:** https://redux-toolkit.js.org
- **React Query:** https://tanstack.com/query
- **Jotai:** https://jotai.org
- **Recoil:** https://recoiljs.org
