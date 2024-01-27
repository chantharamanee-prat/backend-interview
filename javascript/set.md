## Set

In JavaScript, a `Set` is a built-in object that allows you to store unique values of any data type, whether they are primitive values or object references. Unlike arrays or objects, a `Set` only stores distinct elements, ensuring that each element appears only once. The `Set` object is useful when you need to work with a collection of unique values or perform operations like adding, removing, and checking for the existence of elements efficiently.

Here are the key characteristics of a `Set`:

1. **Unique Values:**
   - A `Set` can only contain unique values. If you attempt to add a duplicate value, it won't be added, and the set remains unchanged.

2. **Data Types:**
   - Elements in a `Set` can be of any data type, including numbers, strings, booleans, objects, and even other `Set` instances.

3. **No Indexing:**
   - Unlike arrays, `Set` objects don't have indexes for accessing elements. You cannot directly access elements by their position in the `Set`.

4. **Ordering:**
   - While a `Set` does maintain the order of insertion, it doesn't provide direct indexing or positioning of elements like an array.

5. **Size:**
   - You can easily get the number of elements in a `Set` using its `size` property.

6. **Methods:**
   - `add(value)`: Adds a new unique value to the `Set`.
   - `delete(value)`: Removes a value from the `Set`.
   - `has(value)`: Returns a boolean indicating whether the specified value exists in the `Set`.
   - `clear()`: Removes all elements from the `Set`.
   - `values()`: Returns an iterator over the values in the `Set`.

7. **Example:**
   ```javascript
   // Creating a Set
   const mySet = new Set();

   // Adding values
   mySet.add(42);
   mySet.add('John');
   mySet.add({ key: 'value' });

   // Checking existence
   console.log(mySet.has(42)); // Output: true

   // Deleting a value
   mySet.delete('John');

   // Iterating over values
   for (const value of mySet.values()) {
     console.log(value);
   }
   ```

The `Set` object provides a straightforward way to handle collections of unique values without worrying about duplicates. It's especially useful when you need to perform set-related operations like union, intersection, and difference, as it offers a convenient API for working with such sets of values.