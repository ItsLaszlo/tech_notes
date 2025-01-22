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


### Component Pattern

Import
Function
Export: makes function/COMPONENT available to other modules
\*\*\*\*\*\*\*\*\*\*

### Hook

A way to use Reacts featured insde of a component

\*\*\*\*\*\*\*\*\*\*
---

## GETTING STARTED COMMANDS


`npm install`  
`install` show all containers

\*\*\*\*\*\*\*\*\*\*

### COMMAND

`npm run dev`  
`-`

\*\*\*\*\*\*\*\*\*\*

### COMMAND1

``  
`-`

\*\*\*\*\*\*\*\*\*\*

---

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
