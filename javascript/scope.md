## Scope
In JavaScript, scope refers to the context in which variables are declared and accessed. It determines the visibility and accessibility of variables and functions within different parts of your code.

There are two main types of scope in JavaScript:

1. **Global Scope:**
   - Variables declared outside of any function or block have global scope.
   - They can be accessed from any part of the code, including inside functions.

   ```javascript
   var globalVariable = 10;

   function myFunction() {
     console.log(globalVariable); // Accessible inside the function
   }
   ```

2. **Function Scope:**
   - Variables declared inside a function or block have local scope.
   - They are only accessible within that specific function or block.

   ```javascript
   function myFunction() {
     var localVariable = 20; // Local variable
     console.log(localVariable); // Accessible inside the function
   }

   console.log(localVariable); // Error: localVariable is not defined
   ```

3. **Block Scope:**

JavaScript has function scope, which means that each function creates its own scope. However, starting from ECMAScript 6 (ES6), the `let` and `const` keywords introduce block-scoping, which means that variables declared with `let` or `const` are limited to the block (enclosed by curly braces) where they are defined.

```javascript
function exampleScope() {
  if (true) {
    var x = 5; // Function-scoped
    let y = 10; // Block-scoped
    const z = 15; // Block-scoped
  }

  console.log(x); // Accessible (function-scoped)
  console.log(y); // Error: y is not defined (block-scoped)
  console.log(z); // Error: z is not defined (block-scoped)
}
```

Understanding scope is crucial for writing maintainable and bug-free code, as it helps prevent unintended variable conflicts and ensures that variables are used where they are intended to be used.