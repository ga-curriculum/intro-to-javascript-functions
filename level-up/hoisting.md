# Intro to JavaScript Functions - Level Up - Hoisting

![Hero image](./assets/hero-hoisting.png)

Function declarations (and, by extension, arrow functions) cannot be invoked before they are defined. 

In contrast, function declarations are *hoisted* to the top of their scope and may be invoked even if defined later in the code.

Consider the following example: 
```javascript
// This works!
declarationAdd(5, 10);

// This breaks!
expressionAdd(5, 10);

function declarationAdd(a, b) {
  return a + b;
}

const expressionAdd = function(a, b) {
  return a + b;
}
```

> 📚 When your code is run, JavaScript takes a first pass at it to identify all the variables and function declarations. Variables are set up but not assigned their values during this first pass, and entire function declarations are moved to the top. This is referred to as *hoisting*.
