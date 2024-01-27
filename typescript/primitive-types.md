## Primitive Types

In TypeScript, like in JavaScript, primitive types are basic data types that represent simple values. TypeScript has several built-in primitive types, which include:

1. **number:** Represents numeric values, including integers and floating-point numbers.

   ```typescript
   let age: number = 25;
   ```

2. **string:** Represents sequences of characters (text).

   ```typescript
   let name: string = "John";
   ```

3. **boolean:** Represents true or false values.

   ```typescript
   let isStudent: boolean = true;
   ```

4. **null and undefined:** These are special types that have only one value each: `null` and `undefined`, respectively.

   ```typescript
   let data: null = null;
   let status: undefined = undefined;
   ```

5. **symbol:** Represents a unique and immutable value that may be used as an identifier for object properties.

   ```typescript
   let id: symbol = Symbol("id");
   ```

6. **bigint:** Represents whole numbers larger than 2^53 - 1.

   ```typescript
   let bigNumber: bigint = 9007199254740991n;
   ```

These primitive types are the foundation for creating more complex data structures in TypeScript. TypeScript also has other non-primitive types like arrays, objects, functions, and custom-defined types, which allow you to structure and organize your code more effectively.