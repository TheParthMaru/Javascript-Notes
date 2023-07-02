# Execution Context

- Once the code is finished compilated, it goes to execution where global execution context is created for Top-Level Code.

- Top level code is any code which is not inside the function.

- So in the beginning, only the code which is outside the functions is executed which makes sense as code inside a function needs to be executed only when it is called.

- Functions will be declared but the code inside the functions will only execute when it will be called.

- Execution context is an environment in which a piece of JS is executed.

- It stores all the necessary information for the code to be executed such as local variables, args for functions, etc.

- JS code always runs inside an execution context.

- We only have one execution context which is the default context created for the code that is not inside any fucntion (top level).

- Once the top level code is executed, execution of functions and waiting for callbacks starts.

- For each and every function call, a new EC is created.

- This also applies for methods which are functions attached to objects.

- Thus, we have one EC per function.

- All together makes a call stack.

- When all the functions are done executing, the engine waits for the callback functions to arrive from the callback queue. 

- The event loop provide these callback functions from the callback queue to the call stack.

# Inside of EC

- Variable environments
  
  - let, const, var declarations
  
  - Functions declaration
  
  - Argument objects (contains all the arguments passed to the functions of the current EC)

- Scope chain
  
  - Consists of references of variables that are outside of the functions.

- `this` keyword

- All this is created during creation phase right before execution. 

- EC generated for arrow functions do not get their args object and this keyword.

![](C:\Users\parth\AppData\Roaming\marktext\images\2023-07-02-10-27-43-image.png)

![](C:\Users\parth\AppData\Roaming\marktext\images\2023-07-02-10-30-05-image.png)

- `second()` -> `first()` -> `Global` execution order.

- 
