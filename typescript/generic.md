## Generic

Let's dive into the concepts of generic types and generic constraints in TypeScript.

### Generic Types:

**Generic types** in TypeScript allow you to create functions, classes, and interfaces that can work with different data types while maintaining type safety. They provide a way to write flexible and reusable code.

Here's a simple example of a generic function:

```typescript
function identity<T>(arg: T): T {
    return arg;
}

// Usage
let result1: number = identity(5);       // T is inferred as number
let result2: string = identity("hello"); // T is inferred as string
```

In this example, `identity` is a generic function that can accept any type (`T`). The type parameter `T` is determined at the time of calling the function.

### Generic Constraints:

**Generic constraints** allow you to restrict the types that can be used with a generic function, class, or interface. This is useful when you want to ensure that certain operations are valid for the provided types.

Here's an example of a generic function with a constraint:

```typescript
interface Printable {
    print(): void;
}

function printItem<T extends Printable>(item: T): void {
    item.print();
}

// Usage
class Book implements Printable {
    print(): void {
        console.log("Printing a book.");
    }
}

let myBook = new Book();
printItem(myBook); // Valid, because Book implements Printable

// This would be an error, as a number does not implement Printable
// printItem(42); 
```

In this example, the `printItem` function takes a generic type `T` that must extend (`extends`) the `Printable` interface. This ensures that only types with a `print` method can be passed to the function.

To summarize:

- **Generic Types** allow you to write functions, classes, and interfaces that work with different types.
- **Generic Constraints** enable you to restrict the types that can be used with a generic, providing more control and type safety.

Generics are a powerful feature in TypeScript, promoting code reusability and maintaining strong type checking. They are commonly used in libraries and frameworks to create flexible and type-safe APIs.