# Basics of JS
### 1. var 
- var variables can be re-declared and updated. 
```js
var greeter = "hey hi"; 
var greeter = "say Hello instead";
```
- While this is not a problem if you knowingly want a variable to be redefined, it becomes a problem when you do not realize that the same has already been defined before.

- Hoisting of var 
Hoisting is a JavaScript mechanism where variables and function declarations are moved to the top of their scope before code execution.
```js
 console.log (greeter);
var greeter = "say hello";

//gets interpreted as
var greeter;
console.log(greeter); // greeter is undefined
greeter = "say hello"
```
So var variables are hoisted to the top of their scope and initialized with a value of undefined.

### 2. let 
- let is block scoped. Using variable outside its block (the curly braces where it was defined) returns an error.
- let can be updated but not re-declared. 
```js
let greeting = "say Hi";  
greeting = "say Hello instead";     // works

let greeting = "say Hi"; 
let greeting = "say Hello instead"; // error: Identifier 'greeting' has already been declared
```
- Hoisting of let
Just like  var, let declarations are hoisted to the top. Unlike var which is initialized as undefined, the let keyword is not initialized. So if you try to use a let variable before declaration, you'll get a Reference Error.

### 3. const
- const declarations are block scoped.
- const cannot be updated or re-declared. 
- Hoisting of const : Just like let, const declarations are hoisted to the top but are not initialized.
- While var and let can be declared without being initialized, const must be initialized during declaration.

