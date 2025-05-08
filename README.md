1. What are some differences between interfaces and types in TypeScript?

Both type and interface are used to define the structure of data or describe the shape of an object and bring more clarity to the code but they have some differences

Declaration Merging:
Interfaces support declaration merging, meaning that multiple interfaces with the same name in the same scope will be merged into a single interface. Types do not support this.
Flexibility:
Types are more versatile and can define things like primitive types, unions, and intersections, which interfaces cannot directly represent.
Extensibility:
Both interfaces and types can be extended. Interfaces use the extends keyword, while types use intersection types (&).
Use Cases:
Interfaces are typically used to define the structure of objects and class contracts, while types are better suited for more complex type manipulations and representing non-object types.
Error messages:
Interfaces are considered to provide better (more readable) error messages than types.
TypeScript

// Declaration Merging (Interfaces)
interface Person {
  name: string;
}

interface Person {
  age: number;
}

// Result: Person interface now has both name and age properties

// No Declaration Merging (Types)
type Animal = {
  name: string;
};

// type Animal = { // Error: Duplicate identifier 'Animal'.
//   age: number;
// };

// Unions and Intersections (Types)
type StringOrNumber = string | number;
type PersonAndAddress = Person & { address: string };

// Extending (Interfaces and Types)
interface Employee extends Person {
  employeeId: number;
}

type Manager = Person & {
  manages: Employee[];
};

2. How does TypeScript help in improving code quality and project maintainability?
   Typescript was invented as a solution to the lacking of Javascript. This language is based on javascript but has some extra ficilites.
-> TypeScript catches errors before we run the code.
   this feature helps to identify the erroe while writing so bag fixing becomes easier and user do not have to find error after running the whole project. This feature saves a lot of time.
-> The typescript gives data type safety
   In typescript, we can define what kind of data each variable, function, or object should have. This makes our code more readable, especially for teammates or our future self.
-> Helps with Better Autocomplete and Suggestions
With types defined, your editor (like VS Code) can give you smart suggestions, autocomplete, and even documentation right inside your code. This makes you faster and more confident when coding.
-> Keeps Large Projects Organized
In big projects, it’s easy to lose track of what each part does. TypeScript makes it easier to manage your files, types, and logic. You can create shared types that everyone on the team uses, and the compiler will make sure no one breaks the rules.

TypeScript might seem a bit strict at first, but once you get used to it, you’ll realize it actually makes your work easier. It helps you write better code, catch mistakes early, and work faster with your team.
So if you're working on a project—big or small—TypeScript is a smart choice to keep everything clean and bug-free.
