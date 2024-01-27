## Object Types

Let's go through each of these TypeScript concepts:

1. **Interface:**
   - An interface in TypeScript is a way to define a contract for an object's structure. It specifies the names and types of properties or methods an object should have.
   - Example:

     ```typescript
     interface Person {
       name: string;
       age: number;
       sayHello(): void;
     }

     let person: Person = {
       name: "John",
       age: 25,
       sayHello() {
         console.log("Hello!");
       },
     };
     ```

2. **Class:**
   - A class is a blueprint for creating objects with specific properties and methods. It is a fundamental concept in object-oriented programming (OOP).
   - Example:

     ```typescript
     class Animal {
       name: string;

       constructor(name: string) {
         this.name = name;
       }

       makeSound() {
         console.log("Some generic sound");
       }
     }

     let cat = new Animal("Whiskers");
     cat.makeSound(); // Outputs: Some generic sound
     ```

3. **Enum:**
   - Enums in TypeScript are used to define a set of named numeric constants. They make code more readable and self-documenting.
   - Example:

     ```typescript
     enum Color {
       Red,
       Green,
       Blue,
     }

     let selectedColor: Color = Color.Green;
     console.log(selectedColor); // Outputs: 1 (the numeric value of Green)
     ```

4. **Arrays:**
   - Arrays in TypeScript are used to store collections of values. You can define an array using a specific type or a combination of types.
   - Example:

     ```typescript
     let numbers: number[] = [1, 2, 3, 4];
     let names: string[] = ["John", "Jane", "Doe"];
     ```

5. **Tuples:**
   - Tuples are arrays with a fixed number of elements where each element has a specific type. They allow you to express an array where the type of a fixed number of elements is known.
   - Example:

     ```typescript
     let person: [string, number] = ["John", 25];
     ```

These concepts are fundamental to understanding and writing TypeScript code. Interfaces and classes help you define and work with complex data structures, enums provide named constants, and arrays and tuples are used for collections of values.