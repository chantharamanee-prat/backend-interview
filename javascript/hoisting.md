## Hoisting
In JavaScript, hoisting is a behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use variables or functions before they are declared in your code.

Let's look at examples of variable and function hoisting:

1. **Variable Hoisting:**
   ```javascript
   console.log(x); // Output: undefined
   var x = 5;
   console.log(x); // Output: 5
   ```
   Even though `console.log(x)` appears before the variable `x` is declared, JavaScript "hoists" the declaration to the top, making it `undefined` at the first log and then assigning `5` later.

2. **Function Hoisting:**
   ```javascript
   sayHello(); // Output: "Hello!"
   function sayHello() {
     console.log("Hello!");
   }
   ```
   The function `sayHello` is hoisted to the top, allowing you to call it before its actual declaration in the code.

It's important to note that only the declarations are hoisted, not the initializations. For variables, the declaration is hoisted, but the assignment stays in place. For functions, both the declaration and the function body are hoisted.

Here's an example that illustrates this point:

```javascript
console.log(y); // Output: undefined
var y = 10;
console.log(y); // Output: 10

// Function declaration
hoistedFunction(); // Output: "I am hoisted!"
function hoistedFunction() {
  console.log("I am hoisted!");
}
```

Understanding hoisting helps developers write cleaner code by placing declarations at the top of their scope and can also prevent unexpected behavior caused by hoisting.