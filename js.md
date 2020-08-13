# Javascript

### Variables 

```js
// 3 ways to make variables
var hi = "hello"
let hi = "hello" // let is more tightly scoped
const hi = "hello" //consts can't change, saves memory
```

**Variable Types**
```js
// Simple Types
let hi = "hello" // string
let num = 10 // number
let bool = true // boolean

// Compound Types (you can mix and match types)
let arr = [1, 2, 3, "hi"] // array
arr[3] // returns "hi
let obj = {
    hi: "hello",
    num: 1001,
    bool: false,
    funky: function() {
        // you can even put functions inside
    }
}
obj.funky() // runs the funky function
obj.num // returns 1001
obj["n"] // also returns 1001

// Functions are also Variables!
var funky = function() {
    console.log("a funky function")
}
```

### Functions
```js
//Functions returns an answer (but not all functions need to return something)
//this functions has 2 arguments, "a" and "b"
function add(a, b) {
    return a+b;
}
//calling a function (and passing in 2 values)
//now c equals 3
var c = add(1, 2)

//Fat Arrow Syntax (means return)
//Identical to the add function
//Don't have to type the word "function"
var add2 = (a, b) => a+b;
```

### Loops
```js
for (let i = 0; i < 100; i++) {
    console.log(i) //will print every number between 0 and 1
}

// .map — used in React all the time
[1, 2, 3].map((n, i) => console.log(n, i))
```

### If Statements
```js
if (3 === 2) {
    console.log("nope")
} else {
    console.log("yes")
}

if (3 === 3) {
    console.log("yes")
}

if (3 == "3") { // only compares value
    console.log("yes")
}

if (3 === '3') { // === compares value AND type
    console.log("nope")
}

if (true && false) { // and
    console.log("nope")
}

if (true || false) { //or
    console.log("yes")
}
// Ternary Expression
var n = 2=="2" ? 10 : "hello"
```

// Ternary expressions are useful in React to make dynamic props
```jsx
<div style ={{
    color: theme.dark ? "white" : "black"
}} />

// or for dynamically rendering components
function Header() {
    const [settings, setSettings] = useState(false)
    return <div>
        { settings ? 
            <SettingsMenu /> :
            <ToggleButton />
        }
    </div>
}

// && is used a lot in React. In this example, SettingsMenu will only render if "settings" is true. (! means "not")
const [settings, setSettings] = useState(true)
return <div>
    {settings && <SettingsMenu />}
    {!settings && <ToggleButton />}
</div>
```