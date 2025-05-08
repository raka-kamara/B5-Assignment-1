1. What are some differences between interfaces and types in TypeScript?

Both type and interface are used to define the structure of data or describe the shape of an object and bring more clarity to the code but they have some differences

Basic syntax:

interface User {
  name: string;
  age: number;
}

type User = {
  name: string;
  age: number;
};
They look similar but the differences are described here ->


Feature	                           Interface	                         Type Alias
Extensibility	           ✔️ Can be extended or reopened	         ❌ Cannot be reopened
Composition	                       Limited	                      ✔️ Supports unions and intersections
Implements (classes)	        ✔️ Best fit	                        ✔️ Also supported
Readability in IDEs	         High (often clearer)	                 Moderate
Use in utility types	          Moderate	                     ✔️ Highly compatible


2. How does TypeScript help in improving code quality and project maintainability?
   Typescript was invented as a solution to the lacking of Javascript. This language is based on javascript but has some extra ficilites.
-> Typecsript catches errors before we run the code.
   this feature helps to identify the erroe while writing so bag fixing becomes easier and user do not have to find error after running the whole project. This feature saves a lot of time.
-> Typescript gives data type safety
   In typescript, we can define what kind of data each variable, function, or object should have. This makes our code more readable, especially for teammates or our future self.
-> Helps with Better Autocomplete and Suggestions
With types defined, your editor (like VS Code) can give you smart suggestions, autocomplete, and even documentation right inside your code. This makes you faster and more confident when coding.
-> Keeps Large Projects Organized
In big projects, it’s easy to lose track of what each part does. TypeScript makes it easier to manage your files, types, and logic. You can create shared types that everyone on the team uses, and the compiler will make sure no one breaks the rules.

TypeScript might seem a bit strict at first, but once you get used to it, you’ll realize it actually makes your work easier. It helps you write better code, catch mistakes early, and work faster with your team.
So if you're working on a project—big or small—TypeScript is a smart choice to keep everything clean and bug-free.
