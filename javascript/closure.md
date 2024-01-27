## Closure

In JavaScript, a closure is a combination of a function and the lexical environment within which that function was declared. This lexical environment consists of the variables and their values that were in scope at the time the closure was created. In simpler terms, a closure allows a function to retain access to the variables from its outer (enclosing) scope even after the outer function has finished execution.

Here's a basic example to illustrate closures:

```javascript
function outerFunction() {
  let outerVariable = "I am from the outer function";

  function innerFunction() {
    console.log(outerVariable); // Accessing outerVariable from the outer scope
  }

  return innerFunction;
}

// Create a closure by calling outerFunction
const closure = outerFunction();

// Execute the closure, which still has access to outerVariable
closure(); // Outputs: "I am from the outer function"
```

In this example, `outerFunction` declares a variable called `outerVariable`, and within it, there's another function called `innerFunction`. The `innerFunction` is returned from `outerFunction`. When `outerFunction` is called and assigned to `closure`, it creates a closure where `innerFunction` still has access to `outerVariable`, even though `outerFunction` has already finished executing.

Closures are powerful and flexible in JavaScript, often used to create private variables, maintain state between function calls, and implement various design patterns. They play a crucial role in functional programming and can be seen in many JavaScript frameworks and libraries.