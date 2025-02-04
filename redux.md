# Redux

State management library for JS apps. Manages global state in applications where multiple components need access to shared state  
**Manages and updates state**

## Key Terms

### Store

Holds the entire application state  
#### `createStore`  
Redux function used to create Redux store
```ts
const store = createStore(
  reducers,            // Root reducer function
  {},                  // Initial state (empty object here)
  applyMiddleware(thunk) // Apply middleware (e.g., thunk for async actions)
);

```

### Action Creator

Function that returns an action


\*\*\*\*\*\*\*\*\*\*



### Middleware  

Middleware is code that intercepts actions before they reach the reducer  
\*\*\*\*\*\*\*\*\*\*

---

## Methods

### `dispatch`

Sends actions to the Redux store/Reducer. When called it tells Redux to update the state based on the action passed through it. -> Reducer looks at action type to see how to change state

### Reducer

Function that defines how the state changes after an action  
\*\*\*\*\*\*\*\*\*\*

\*\*\*\*\*\*\*\*\*\*

### React + Redux

#### `<Provider>`
Wrapper component that makes redux store available to all nested components in the app. Gives access to the global state managed by Redux.


\*\*\*\*\*\*\*\*\*\*

### `useDispatch`
Hook that gives access to dispatch function

``  
`-`

\*\*\*\*\*\*\*\*\*\*

---

## ADVANCED COMMANDS

### COMMAND2

``  
`-`

\*\*\*\*\*\*\*\*\*\*

### COMMAND3

``  
`-`

\*\*\*\*\*\*\*\*\*\*

---

## Configs

### Name_of_config

What does the config do  
Config example and definition of each term

\*\*\*\*\*\*\*\*\*\*

---

## Processes

### Process

1. steps
2. step
3. step

\*\*\*\*\*\*\*\*\*\*

---

## Links

[Name](link)  
