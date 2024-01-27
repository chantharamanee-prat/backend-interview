## Asynchronous

### Table of contents
1. [Callback](#callback)
2. [Promise & Async / Await](#promise--async--await)


### Callback
In JavaScript, a callback is a function that is passed as an argument to another function and is executed after the completion of some asynchronous operation or a specific event. Callbacks are a fundamental concept in asynchronous programming and are often used to handle tasks that take time to complete, such as fetching data from a server, reading a file, or handling user interactions.

Here's a simple example to illustrate the concept of a callback:

```javascript
// Function that takes a callback
function fetchData(callback) {
  // Simulating an asynchronous operation (e.g., fetching data)
  setTimeout(function () {
    const data = "This is the fetched data";
    // Calling the callback with the fetched data
    callback(data);
  }, 2000); // This will wait for 2 seconds
}

// Callback function to handle the fetched data
function handleData(data) {
  console.log("Data received:", data);
}

// Calling the fetchData function with the handleData callback
fetchData(handleData);

console.log("Continuing with other tasks");
```

In this example, `fetchData` is a function that simulates fetching data asynchronously. It takes a callback function (`handleData`) as an argument. After the asynchronous operation (here, a `setTimeout` to simulate waiting for 2 seconds), the callback function is invoked with the fetched data.

Callbacks are powerful in handling asynchronous code because they allow you to specify what should happen after a particular operation is completed, without blocking the rest of the code. They are widely used in scenarios like event handling, AJAX requests, and more.

However, as code grows, using callbacks can lead to a pattern known as "callback hell" or "pyramid of doom," where nested callbacks make the code hard to read and maintain. To address this, modern JavaScript introduces features like Promises and async/await, which provide cleaner ways to handle asynchronous operations.

### Promise & Async / Await

Certainly! In JavaScript, a `Promise` is an object that represents the eventual completion or failure of an asynchronous operation and its resulting value. It's a way to handle asynchronous code in a more structured and readable manner.

Here's a simple breakdown:

1. **States of a Promise:**
   - **Pending:** The initial state. The promise is neither fulfilled nor rejected.
   - **Fulfilled:** The operation completed successfully, and the promise has a resulting value.
   - **Rejected:** The operation failed, and the promise has a reason for the failure.

2. **Creating a Promise:**
   You create a promise using the `Promise` constructor. It takes a function as an argument, commonly referred to as the "executor" function. This function receives two parameters: `resolve` and `reject`. You use these functions to indicate the success or failure of your asynchronous operation.

   ```javascript
   const myPromise = new Promise((resolve, reject) => {
     // Your asynchronous operation here
     // If successful, call resolve with the result
     // If failed, call reject with the reason
   });
   ```

3. **Handling Promises:**
   You can use `.then()` and `.catch()` methods to handle the results (fulfillment) or errors (rejection) of a promise.

   ```javascript
   myPromise
     .then(result => {
       // Handle successful result
     })
     .catch(error => {
       // Handle error
     });
   ```

4. **Chaining Promises:**
   You can chain multiple asynchronous operations together using `.then()`. Each `.then()` returns a new promise.

   ```javascript
   myPromise
     .then(result => {
       // First operation
       return anotherAsyncOperation(result);
     })
     .then(newResult => {
       // Second operation
     })
     .catch(error => {
       // Handle errors in any of the operations
     });
   ```

5. **Async/Await:**
   ES2017 introduced `async/await`, which is a syntactic sugar for working with promises. It makes asynchronous code look more like synchronous code, making it easier to read and write.

   ```javascript
   async function myAsyncFunction() {
     try {
       const result = await myPromise;
       // Handle the result
     } catch (error) {
       // Handle errors
     }
   }
   ```

Promises are widely used in modern JavaScript, especially in scenarios like making network requests, reading files, or handling other asynchronous tasks. They provide a more organized and readable way to work with asynchronous code compared to using callbacks alone.