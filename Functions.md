# Functions

- Block of reusable code.

## Syntax of functions

```js
// Function definition
function functionName(parameter1, parameter2, ...) {
    // statements
    return;
}

// Function call
functionName(argument1, argument2, ...);
```

- All the variables and constants declared inside the function belongs to that function.
- Function parameters are optional and return is also optional.
- Function can be called multiple times with different arguments.
- Function can be called directly or indirectly.

## Function in an object

- We can store a function in an object.
- A function associated with an object is called as a Method.

```js
const person = {
  greet: function greetMessage() {
    console.log("Hello");
  },
};

person.greet(); // Hello

console.log(person.greet); // [Function: greetMessage]
```

- Functions are also considered as objects in JS.

```js
function greet() {
  console.log("Good morning");
}

console.log(typeof greet); // Function
```

- `Function` is also a type.

#### Note:

```js
// In Firefox
console.log(functionName); // Prints toString()
console.dir(functionName); // Tree like expandable structure

// In chrome
console.log(functionName); // Displays function definition
console.dir(functionName); // Tree like expandable structure
```

## Function expression

- Storing a function in a variable or a constant.

```js
const greetUser = function greeting(name) {
  console.log("Hi " + name);
};

greetUser("Parth"); // Hi Parth

console.log(greetUser); // [Function: greeting]
console.log(typeof greetUser); // function

greeting("Parth"); // Error, greeting is not defined as an object.<anonymous>

// So we can omit the greeting word that is function name as we are using variable name to call the function.

// Anonymous function
const greetUser = function (name) {
  console.log("Hello " + name);
};

greetUser("Parth"); // Hello Parth
```

## Function declaration vs Function expression

```js
// Function declaration
function add(a, b) {
  return a + b;
}
```

- When we use function declaration, they are hoisted to the top even though they are declared anywhere in the file.
- We can call them before declaration.
- If your code style is to keep all the functions at the bottom of the code, you can use function declaration style.

```js
// Function expression
const add = function (a, b) {
  return a + b;
};
```

- Hoisted to the top but not initialized or defined.
- We can't declare them anywhere in the file and call before declaration.
- We get `ReferenceError: Cannot access 'functionName' before initialization` error when we call the function expression before declaring it.

## Anonymous function
