# Intro to JS Functions - Declaration, Expression, and Scope

![Hero image](../assets/tktkhero-secondary-subhead.png)

**Learning objective:** By the end of this lesson, students will be able to compose function declarations and function expressions with appropriate syntax and naming conventions, and have a clear understanding of function scope.

## Function Expressions: Assigning a function to a variable

So far, we've mostly covered function declarations, but it's important to be aware of another fundamental way of writing a function: function expressions. 

Let's look at an example function declaration: 

```javascript
function add(a, b){
  return a + b;
}
```

The same function, as a function expression, would look like this:

```javascript
const add = function(a, b) {
  return a + b;
}
```
The `function` keyword is used to define a function inside of the expression.  

Note that the function itself has no name - function expressions allow us to omit the name and create what is known as an _anonymous function_.

Another key difference is that function expressions cannot be invoked before they are defined. In contrast, function declarations are **hoisted** to the top of their scope and may be invoked even if they are defined later in the source code.

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


## Scope

A function creates its own scope, which means that a variable defined within a function cannot be accessed from outside the function. 

> 🧠 Variables created inside any scope other than global scope are considered to be **locally scoped**.

There are two primary considerations when working with function scope. The first has to do with parameters. Parameters are locally scoped variables, which means they will not be accessible outside of the function body in which they are created. 

For example:

```javascript
const sayHello = function(name){
  console.log(name); // Ben! 
}

sayHello('Ben');

console.log(name); // undefined! name is not defined outside of the function body.
```

<br>

Secondly, variables that are initialized inside the function body are also locally scoped: 

```javascript
const sayHello = function(name){
  const fullGreeting = 'Hi, my name is ' + name + '!';
  console.log(fullGreeting);  // Hi, my name is Gretta! 
}

sayHello('Gretta');

console.log(fullGreeting); // undefined again! 

```

The positives to function scope are that the variables we create solely for use in a function don't pollute our global scope.
This means that we can reuse parameter and variable names without concern: 

```javascript
const add = function(num1, num2){
  const total = num1 + num2;
  return total;
}

const subtract = function(num1, num2){
  const total = num1 - num2;
  return total;
}
```

No problems - thanks function scope! 



## Functions - Review Questions ❓

**❓ What’s the only practical difference between a function definition and a function expression?**

### Given this code:

```javascript
function sumTwoNumbers(numA, numB){
  return numA + numB
}

const sum = sumTwoNumbers(5, 10)
```

1. What is the job of the `sumTwoNumbers` function?
1. Is `numA` a parameter or an argument?
1. What will the value of `numA` be inside the `sumTwoNumbers` function?
1. Will `numA` have a value outside of the `sumTwoNumbers` function?
1. What data type will the value returned from the `sumTwoNumbers` function be?
1. What will be returned from the `sumTwoNumbers` function?
1. What would the value of `sum` be if we console logged it after the final line?
1. How many arguments are passed to the `sumTwoNumbers` function? What are they?
1. How many parameters does the `sumTwoNumbers` function accept? What are they?

### Given this code:

```javascript
function emphasize(string){
  return string + ' ' + string + '!'
}

emphasize('really')
```

1. What does the `emphasize` function do?
1. What will the value of `string` be inside of the `emphasize` function?
1. What will be returned from the `emphasize` function?
1. What data type will the value returned from the `emphasize` function be?
1. Will what is returned from the `emphasize` function be usable later on in this program? If not, how could we make it so that it is?
1. How could we make it so that what is returned from the `emphasize` function is shown in the console?
1. How many arguments are passed to the `emphasize` function? What are they?
1. How many parameters does the `emphasize` function accept? What are they?