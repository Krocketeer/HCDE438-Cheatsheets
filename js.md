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