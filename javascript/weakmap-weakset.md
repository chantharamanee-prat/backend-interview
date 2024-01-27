## WeakMap & WeakSet

In JavaScript, `WeakMap` and `WeakSet` are object collections with some distinctive characteristics related to garbage collection and memory management.

### WeakMap:

A `WeakMap` is a collection of key-value pairs where the keys must be objects, and the values can be arbitrary values. The key distinction is that the references to the keys in a `WeakMap` are weak, meaning they do not prevent the keys from being garbage-collected if there are no other references to them.

#### Characteristics:

1. **Key Weak References:**
   - Unlike regular `Map`, the keys in a `WeakMap` are held by weak references. If there are no other references to a key, it may be garbage-collected, and the corresponding entry in the `WeakMap` is automatically removed.

2. **No Iteration:**
   - You cannot iterate over the keys or values of a `WeakMap` directly. It does not expose any method for obtaining a list of keys or values.

3. **Limited API:**
   - The API of `WeakMap` is intentionally limited. It only provides methods like `set(key, value)`, `get(key)`, `has(key)`, and `delete(key)`.

#### Example:

```javascript
// Creating a WeakMap
const weakMap = new WeakMap();

// Creating objects to be used as keys
const key1 = { id: 1 };
const key2 = { id: 2 };

// Adding entries
weakMap.set(key1, 'Value associated with key1');
weakMap.set(key2, 'Value associated with key2');

// Retrieving values
console.log(weakMap.get(key1)); // Output: Value associated with key1

// Checking existence
console.log(weakMap.has(key2)); // Output: true

// Deleting entry
weakMap.delete(key1);
console.log(weakMap.has(key1)); // Output: false
```

### WeakSet:

A `WeakSet` is a collection of objects where each object must be unique. Similar to `WeakMap`, the references to the objects in a `WeakSet` are weak, meaning they do not prevent the objects from being garbage-collected if there are no other references to them.

#### Characteristics:

1. **Weak Object References:**
   - The objects in a `WeakSet` are held by weak references. If there are no other references to an object, it may be garbage-collected, and the corresponding entry in the `WeakSet` is automatically removed.

2. **No Iteration:**
   - Similar to `WeakMap`, you cannot iterate over the values of a `WeakSet`. It does not provide methods for obtaining a list of values.

3. **Limited API:**
   - The API of `WeakSet` is intentionally limited. It only provides methods like `add(value)`, `has(value)`, and `delete(value)`.

#### Example:

```javascript
// Creating a WeakSet
const weakSet = new WeakSet();

// Creating objects to be used as values
const obj1 = { id: 1 };
const obj2 = { id: 2 };

// Adding objects
weakSet.add(obj1);
weakSet.add(obj2);

// Checking existence
console.log(weakSet.has(obj1)); // Output: true

// Deleting entry
weakSet.delete(obj1);
console.log(weakSet.has(obj1)); // Output: false
```

**Note:** Both `WeakMap` and `WeakSet` are not suitable for all use cases, and their use depends on specific scenarios where the weak references are desired to allow automatic garbage collection. They are commonly used in situations where the additional memory pressure caused by strong references is a concern.