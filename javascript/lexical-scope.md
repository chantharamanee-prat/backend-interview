## Lexical Scope

Lexical scope is a concept in JavaScript that defines how the scope, or the visibility and accessibility of variables, is determined at the time of writing the code (at compile time), based on the physical placement of the variables and blocks of code within the source code. Lexical scope is also referred to as static scope.

In simpler terms, lexical scope means that the scope of a variable is determined by its position within the source code.

Here's a basic example to illustrate lexical scope:

```javascript
function outer() {
  // Variable defined in the outer function
  const outerVariable = 'I am from outer';

  function inner() {
    // Accessing outerVariable from the outer function
    console.log(outerVariable); 
  }

  // Calling the inner function
  inner();
}

// Calling the outer function
outer();
```

In this example, the `inner` function is lexically scoped within the `outer` function. This means that the `inner` function has access to the variables defined in its containing scope (`outer` function), and it can access `outerVariable` directly.

Contrastingly, if we try to access a variable from an inner scope in an outer scope, it won't work:

```javascript
function outer() {
  const outerVariable = 'I am from outer';

  function inner() {
    // Trying to access a variable from the inner function in the outer scope
    console.log(innerVariable); // Error: innerVariable is not defined
  }

  // Defining a variable in the inner function
  const innerVariable = 'I am from inner';

  inner();
}

outer();
```

In this case, the `outer` function cannot access `innerVariable` because it is lexically scoped within the `inner` function.

Lexical scope is powerful because it allows the JavaScript engine to determine the scope of a variable just by looking at the code, which improves predictability and helps developers reason about their code more effectively. It's a fundamental concept in understanding how scope works in JavaScript.