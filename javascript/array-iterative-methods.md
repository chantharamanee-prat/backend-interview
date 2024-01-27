## Array Iterative Methods

Array iterative methods are powerful tools in JavaScript that allow you to traverse and manipulate arrays in a concise and expressive way. These methods make it easier to work with arrays compared to traditional `for` loops. Here are some commonly used array iterative methods:

1. **`forEach`:**
   - **Purpose:** Executes a provided function once for each array element.
   - **Usage:**
     ```javascript
     const numbers = [1, 2, 3, 4];

     numbers.forEach((number, index) => {
       console.log(`Element at index ${index}: ${number}`);
     });
     ```

2. **`map`:**
   - **Purpose:** Creates a new array by applying a function to each element in the original array.
   - **Usage:**
     ```javascript
     const numbers = [1, 2, 3, 4];

     const doubled = numbers.map(number => number * 2);
     console.log(doubled); // [2, 4, 6, 8]
     ```

3. **`filter`:**
   - **Purpose:** Creates a new array with elements that pass a certain condition.
   - **Usage:**
     ```javascript
     const numbers = [1, 2, 3, 4];

     const evens = numbers.filter(number => number % 2 === 0);
     console.log(evens); // [2, 4]
     ```

4. **`find`:**
   - **Purpose:** Returns the first element in the array that satisfies a provided testing function.
   - **Usage:**
     ```javascript
     const numbers = [1, 2, 3, 4];

     const firstEven = numbers.find(number => number % 2 === 0);
     console.log(firstEven); // 2
     ```

5. **`reduce`:**
   - **Purpose:** Applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.
   - **Usage:**
     ```javascript
     const numbers = [1, 2, 3, 4];

     const sum = numbers.reduce((accumulator, current) => accumulator + current, 0);
     console.log(sum); // 10
     ```

6. **`some` and `every`:**
   - **`some`:** Checks if at least one element in the array passes a test.
   - **`every`:** Checks if all elements in the array pass a test.
   - **Usage:**
     ```javascript
     const numbers = [1, 2, 3, 4];

     const hasEven = numbers.some(number => number % 2 === 0);
     console.log(hasEven); // true

     const allEven = numbers.every(number => number % 2 === 0);
     console.log(allEven); // false
     ```

These array iterative methods provide a clean and concise way to perform common operations on arrays, making your code more readable and maintainable. Choose the method that best fits your specific use case.