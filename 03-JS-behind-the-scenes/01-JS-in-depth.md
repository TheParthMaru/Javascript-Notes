# Javascript is High Level

- In JS, resources are managed automatically unlike languages like C/C++.

- The drawback of this is that we won't be able to achieve speed and optimizations like C/C++.

# Garbage Collection

- It is an algorithm inside the JS engine which cleans the memory that is removes unused objects.

- Garbage collector cleans the memory time to time so that we don't have to manually clean it.

# Interpreted or Just-In-Time Compiled

- Converting of a high-level human readable abstract code to machine code (0s and 1s) happens inside JS engine.

# Multi-Paradigm

- Paradigm is an approach or mindset of structuring code which will direct your coding style and technique.

- There are two types of paradigms - Imperative and Declarative.

- Javascript follows:
  
  - Procedural programmming - Organizing the code in a linear way.
  
  - OOP programming - Organizing the code with the help of objects.
  
  - Functional programming - Using functions for all tasks.

# Prototype-based object-oriented

- Almost everything in Javascript is an object except the primitive values.

- Arrays are non-primitive data types.

- We are able to use methods on arrays like `push`, `pop` , etc because arrays are object.

- This is because of prototypal-inheritance.

- We create an array from a blueprint which is called a prototype which contains all the array methods.

- The arrays that we create inherits these methods from the blueprint.

# First class functions

- Functions are treated as variables.

- We can pass functions into another functions and return them from functions.

- This is a powerful feature and enables the use of functional programming.

# Dynamic

- Javascript is a dynamically typed language because we don't explicitly assign data types.

- Data types are assigned at runtime and can be changed later unlike statically typed language like Java, C, C++, etc.

- The disadvantage is that we might get a lot of bugs while coding.

- Statically/Strongly typed languages are more error/bug prone.

# Single threaded

- Javascript only runs on a single thread so it can do only one thing at a time.

- Javascript has adopted concurrency model by using event loop.

- Event loop takes long running tasks, executes them in background and puts them back in the main thread once they are finished.
