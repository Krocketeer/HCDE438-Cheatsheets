# React Cheat Sheet

### Making Components:
```jsx
// A Person component that shows the person's name
function Person(props) {
    return <div style={{fontSize: props.age}}>
        {props.name}
    </div>
}
```

### Use a Component
```jsx
//Here, you render the Person component and pass in the name "alice" in a prop
<Person name="alice" age={30} />
```

### Looping Over Components Using .map()
```jsx
function App() {
    const people=["Alice", "Bob", "Casey", "Diana"]
    return <div>
        {people.map((item, index) => {
            // "key" is something that React needs
            return <Person key={index} name={item} />
        })}
    </div>
}
```

### useState
```jsx
// "state" lets you handle changes on your site in an intelligent way
function Counter() {
    const [count, setCount] = useState(0)
    return <button onClick={() => setCount(count + 1)}>
        You clicked me {count} times!
    </button>
}
```

### Conditionally Rendering Components
```jsx
// You can use && to render a component based on some JavaScript condition
function App() {
    return <div>
        {1 + 1 === 2 && <WillRender />}
        {1 + 1 === 3 && <WontRender />}
    </div>
}

// You can also use "ternary expression" to conditionally render expressions
function App() {
    return <div>
        {1 + 1 === 2 ? <WillRender /> : <WontRender />}
    </div>
}
```

### useEffect
```jsx
function App() {
    useEffect(() => {
        //run some code once on startup
    }, [])
    return <div>hello world</div>
}
```

**or use useEffect more dynamically**

```jsx
function Person(props) {
    useEffect(() => {
        //this code will run EVERY time the person's "age" changes
    }, [props.age])
    return <div>{props.age}</div>
}
```


### Example App
```jsx
import React, {useState, useEffect} from 'react';
import './App.css';

function App() {
  return (
    <div className="App">
      <Counter label="Add One" n={1} initial={5} />
      <Counter label="Minus Two" n={-2} />
      <Counter label="Add 100" n={100} />
    </div>
  )
}

function Counter(props){
  const {label, n, initial} = props
  const [count, setCount] = useState(initial||0)
  return <div style={{marginTop:25}}>
    <button onClick={()=> setCount(count+n)}>
      {label}
    </button>
    <div>
      {count}
    </div>
  </div>
}

export default App;

```

### Other

**React Fragment: <> </> or <React.Fragment> </React.fragment>**
```jsx
// Parentheses for grouping things together in a conditional
{count === 10 && <>
    <a href="google.com">Link</a>
    <br />
</>
}
```