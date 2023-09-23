# Intro the JS Functions - Arrow Function Expressions

![Hero image](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to compose arrow function expressions.

## Arrow Function Expressions

ES2015 (ES6) added a new approach to defining functions - Arrow Function Expressions.

The following function expression:
```javascript
const add = function(a, b) {
  return a + b;
}
```
is equivalent to: 
```javascript
const add = (a, b) => a + b;
```

Arrow Functions offer:

- A more concise syntax - we can leave off the function keyword entirely when composing them.

- Implicit return of a single expression - if an arrow function directly returns an expression, we can leave off the curly braces and the return statement. 

When working with a single parameter, we can also leave off the parentheses entirely: 
```javascript
const double = number => number * 2;
```

Arrow Functions also have a unique way of binding the `this` keyword, which makes them unsuitable for use as methods or constructors - but don’t worry about that for now. Just know, arrow functions exist as a more compact alternative to traditional function expressions. 

## 🧠 You Do: 

Lets practice using this new syntax by converting a regular function into its arrow function equivalent.

1. Take a look at the following function that squares a number:

```JS
function square(num) {
    return num * num;
}
```

1. Convert this function into an arrow function.
2. Could this function be reduced to just one line? What would that look like?


