# Scope

- Accessibility of variables.

- We have lexical scoping in Javascript.

- Lexical scoping is a scoping which is controlled by placement of functions and blocks in the code.

- Scope is a space or an environment in which a certain variable is declared.

- We have global, function and block scope.

- Scope of a variable is the region of our code where a certain variable can be accessed.

## Global scope

- Outside of any function or block.

- Variables declared in global scope are accessed everywhere.

```javascript
const firstName = "parth";
const age = 25;
const profession = "Software Engineer";
```

## Function scope

- Variables are accessible only inside the function and not outside.

- Also called as local scope.

```js
function add(num1, num2) {
    let sum = num1 + num2;
    return sum;
}

console.log(sum); // Reference error
```

## Block scope

- Variables are accessible only inside the block.

- It only applies to variables created using `let` and `const`. 

- Functions are also block scope but only in strict mode.

```js
if(someConditionIsTrue) {
  let favoriteNumber = 69;
  const favoriteDish = "Pav Bhaji";
}

console.log(favoriteNumber, favoriteDish); // ReferenceError
```




