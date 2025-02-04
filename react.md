# React

A library for building user interfaces

## Key Terms

### JSX
 
### Component
Reusable module that renders a part of an overall app. They can be big or small but are clearly defined and serve a single obvious purpose
*Rules:* Use pascal case for functions ex) App, List, AcceptButton

- Component props: A means of passing data into a React component. Props can only be passed from parent components down to child components. Flow of data is unidirectional.
- Attributes: just like HTML attirbutes but different name at times because reserved words in JS
\*\*\*\*\*\*\*\*\*\*


#### Patterns
```
Import
Function
Export: makes function/COMPONENT available to other modules
```
####Types of Components:

- Event: Handle user interactions like clicks, hover, drag bu responding to them and listening to them with built in Event handlers: `onClick` `onChange`.
- Functional: Use functions and react hooks (ex. `useState` `useEffect`) for state and lifecycle methods
- Class: Have state and lifecycle methods built-in. State is declared and uses this to reference it.


\*\*\*\*\*\*\*\*\*\*

### Hooks
Special functions that make components simpler to use by allowing you to keep components cleaner and reuse logic more easily.
#### Types:

- `useState` Add local state to functional components.  
  `const [name,setName] = useState(''); `  
  
      name =  State Variable that holds the current value  
      setName = updates the state
- `useEffect` Use lifecycle methods like mounting, updating, and cleanup.
- `useContext` Access context in a simple way.
- `useRef` Accessing and modifying DOM elements across redenders. Does not trigger a Re-render.

### LifeCycle Events
React component have a life cycle, which consists of three phases:

- Mounting, that is putting inserting elements into the DOM.
- Updating, which involves methods for updating components in the DOM.
- Unmounting, that is removing a component from the DOM.
\*\*\*\*\*\*\*\*\*\*

## NEXT.js Key Terms

### layout.tsx
This file sets up the basic structure for all pages in the Next.js app.

### global.css
This file sets up the basic css structure for all pages in the Next.js app.

### Client Components

### Server Components
UI that can be rendered and optionally cached on the server 
\*\*\*\*\*\*\*\*\*\*

---

## GETTING STARTED COMMANDS


### `npm install`  
`install` show all containers

\*\*\*\*\*\*\*\*\*\*

### `npm run dev`  
`-`

\*\*\*\*\*\*\*\*\*\*
## File structure

### main.jsx
 Entry point of app 

```
import { StrictMode } from 'react'
import { createRoot } from 'react-dom/client' //Finds the specified element where React will inject the app
import './index.css'
import App from './App.jsx'
//.render() Tells React what to display inside the "root element"
createRoot(document.getElementById('root')).render(
  <StrictMode>
    <App />
  </StrictMode>,
)

```


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
