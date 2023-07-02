# Javascript engine

- Basically a computer program that executes Javascript code.

- Every browser has a built-in engine.

- Example is Google's V8 engine which is embedded inside Google Chrome.

- Nodejs is actually V8 engine removed from the browser to work locally.

- Nodejs is neither a library or a framework, but it is a runtime that executes Javascript code outside of browser.

- Any Javascript engine contains a call stack and a heap.

- Call stack is where our code is executed using execution context.

- Heap is a memory pool that stores all our unstructured memory which includes objects.

# Compilation vs Interpretation

- Compilation - The entire source code is converted into machine code at once, and written to a binary file that can be executed by a computer.

- Interpretation - We have an interpreter that runs through the source code and executes it line by line.

- Code still needs to be converted to machine code which happens on the run.

- This makes processing slow and as a result interpreted languages are quite slow compared to compiled languages.

- Javascript was a fully interpreted language but the modern Javascript engine uses a combination of compilation and interpretation which is called as Just-In-Time (JIT) Compilation.

- JIT Compilation - Entire code is converted to machine code at once and then executed immediately.

- The only change is that there is no portable file or binary file.

- The execution happens just after compilation.

- The entire flow is as follows:
  
  - We have the source code with us.
  
  - The JS engine takes this source code and parses it or reads it.
  
  - During the parsing process, the code is parsed into an abstract data structure called the Abstract Syntax Tree (AST).
  
  - This works by splitting the code which are meaningful to the language like keywords and then saving these pieces into the AST in a structured way.
  
  - This step also checks if there are any syntax errors.
  
  - The resulting tree is then used to generate the machine code.
  
  - In short, AST is an entire representation of our code in the engine.
  
  - Next step is compilation of AST into machine code.
  
  - This machine code then gets executed right away as the modern JS uses JIT compilation and no binary file is created.
  
  - Execution happens in Call Stack.
  
  - To make JS execution fast, the machine code which is very unstructured starts getting executed immediately and simultaneously it applies optimizations by compiling it again.
  
  - This happens in already running execution code.
  
  - This happens multiple times and the optimized code is swapped with the unstructured code without ever stopping execution.
  
  - This process makes V8 Engine very fast.
  
  - These process happens in a seperate thread in our call stack which we cannot access through our code.
  
  - Different engines have different implementation but this is how a general JIT compilation works.

# Javascript runtime in browser

- In browser, we have the JS engine which contains the call stack and heap.

- The engine alone is not sufficient so we have the Web APIs (DOM, Timers, Fetch API, etc).

- Web APIs are the functionality provided to the engine which are accessible through the global window objects.

- They are not a part of an engine.

- We also have a callback queue which is a data structure which contains all the callback functions which are ready to be executed.

- When we have an event function and as soon as it is called, it goes to the callback queue and gets stored.

- When the call stack is empty, this onClick event is then put to the call stack from callback queue so that it can be executed.

- This happens through event loop.

- Event loop takes callback functions from the callback queue and puts them in the call stack for execution.

- So to summarize, the Javascript runtime in browser consists of:
  
  - Javascript engine (Call stack + Heap)
  
  - Web APIs (DOM, Timers, Fetch API, etc)
  
  - Callback Queue (click, timers, data, etc)
  
  - Event loop

- For Nodejs we have similar runtime but instead of Web APIs, we have C++ Bindings and Thread Pool.


