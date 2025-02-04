# Typescript

Explanation of the tool and it's purpose. Be Brief and say it concisely in a sentence

## React + typsecript
- File extension `.tsx`
  
## Type Inferencing
- Typescript automatically determins the type of variable based on its assigned value
- In react/jsx only applies this inside JSX when defining callback functions directly in line

### Interfaces

Define structure of an object. Like a contract. 
```TS
interface Person {
  name: string;
  age: number;
}

const person: Person = {
  name: "John",
  age: 30,
};
```
\*\*\*\*\*\*\*\*\*\*

### Define react components in Typescript

```ts
 
export const ChildTwo: React.FunctionComponent<ChildProps> = ({ color, onClick }) => {
  return <div> 
    {color} 
        <button onClick={onClick}>CLIIIICK</button>
    </div>;
};
```

Definition and example  
\*\*\*\*\*\*\*\*\*\*

---

## React

### `React.FunctionComponent` or `React.FC`

It types functional components for TS. It allows component automatically accepts children props and  provides type safety for the props that a component expects to receive.

\*\*\*\*\*\*\*\*\*\*

### COMMAND1

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
