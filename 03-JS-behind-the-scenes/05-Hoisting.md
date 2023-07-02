# Hoisting

- It makes some types of variables accessible before they are actually declared.

- Behind the scenes, before execution, the code is scanned for variable declarations and for each variable, a new property is created in the variable environment object.

- Following things are hoisted in JS:
  
  - Function declaration:
    
    - Initial value - Actual function
    
    - Scope - Block
  
  - `var` variable:
    
    - Initial value - undefined
    
    - Scope - Function
  
  - `let` and `const` variables:
    
    - They are technically not hoisted but instead stored in temporary dead zone (TDZ).
    
    - Initial value - Uninitialized/TDZ
    
    - Scope - Block
  
  - Function expressions and arrows:
    
    - Depends if using `var` or `let/const`.

![](C:\Users\parth\AppData\Roaming\marktext\images\2023-07-02-13-09-10-image.png)

- TDZ makes it easier to avoid and catch errors.

- Accessing variables before declaration is a bad practice and should be avoided.

- Hoisting actually is used for functions.
