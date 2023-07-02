# `this` keyword

- Special variable that is created for every execution context.
- Points to the owner of the function.
- The value is not static.
- It's value depends on how the function is called and its value is only assigned when the function is actually called.

```js
const person = {
  name: "parth",
  year: 1998,
  calcAge: function() {
    return 2037 - this.year;
  }
};

person.calcAge(); // 39
```

- When a method calls `this` keyword, it refers to the object that is calling the method.

- When a simple function calls `this`, it refers to `undefined`.

- When a arrow function calls `this`, it refers to `this` of surrounding function (lexical `this`).

- When a event listener calls `this`, it refers to the DOM element that the handler is attached to.

```javascript
console.log(this); // Returns the window object
```

```javascript
function calcAge(birthYear) {
  console.log(2023 - birthYear); // 25
  console.log(this); // undefined, when in strict mode, else global window object
}
```

```javascript
const calcAge = (birthYear) => {
  console.log(2023 - birthYear); // 25
  console.log(this); // Global window object, because the arrow function does not get its this keyword, so it uses lexical this keyword
  // Which means it uses this keyword of its parent function which is the global function.
}
```

```js
const person = {
  name: "parth",
  age: 25,
  calcAge: function() {
    console.log(this); // Returns the person object, which means person is the owner of calcAge method.
  }
}

person.calcAge();
```

```javascript
const person = {
  firstName: "parth",
  age: 25,
  calcAg: function() {
    console.log(this); // Returns person object
  }
  greet: () => console.log(`Hey ${this.firstName}`), // Calls window object.firstName
};

person.greet(); // Hey undefined

// Since arrow functions do have their own this, they refer to lexical this which in this case will be global function this.
console.log(this.firstName); // undefined
// The above line calls the globa this which is the window object.
// For the window object, we don't have any property named 'firstName'.
// Hence it returns undefined.
```

```js
var firstName = "lily";

const person = {
  firstName: "parth",
  age: 25,
  greet: () => {
    console.log(this); // Prints the window object
    console.log(this.firstName); // lily, because arrow function does not have its own this so it will use global this
    // which is the window object and we have firstName = lily set globally.
  }
} 
```

- The above code clarifies that it is a bad idea to use arrow function as a method.
