# Intro the JS Functions - Return Values

![Hero image](../assets/tktkhero-secondary-subhead.png)

**Learning objective:** By the end of this lesson, students will be able to use the `return` statement to return a value from a function.

## What is a return value

A return value is the output of a function. 

Unless specified, the default return value for a function is `undefined`. Functions are not required to return a defined value, but there are often cases where it is advantageous to use the outcome of running a function for future calculations. This is where the return statement comes in handy.

## The 'return' statement

To return a value from a function, you'll need to use the `return` keyword.

The `return` keyword can only be used inside of functions. When used, it stops the execution of the function, and the function then evaluates to the return value. 

Let's look at some examples: 

```javascript
function addOne(num){
  return num + 1;
}

addOne(3); // 4
```
This works as expected! We are returning the result of adding `num` and 1. 

<br>

```javascript
function addOne(num){
  return 'this is some text';
  return num + 1;
}

addOne(3); // 'this is some text'
```
Here, we see that the first `return` statement blocks the remainder of the code from running! This is because the function stops executing as soon as it hits the first `return` statement.

<br>

```javascript
function addOne(num){
  num + 1;
  return;
}

addOne(3); // undefined
```
Finally, we can see that returning without an expression defaults to `undefined`. 
This is also the case when we omit the `return` statement entirely, as mentioned earlier. 

```javascript
function addOne(num){
  num + 1;
}

addOne(3); // undefined
```


## Storing and using the return value of a function

It is often useful to store the return value of a function. 

Remember, when a function runs, it executes its statements and then returns a value. We can use assignment (the `=` operator) to assign that returned value to a variable, just like any other value. 

For instance, if we wanted to store the value of invoking `addOne()` and passing in 3 as an argument, we could do something like this: 

```javascript
const incrementedNum = addOne(3);

console.log(incrementedNum); // 4
```

For a more involved example, let's imagine we have a shopping cart that needs to calculate tax when the user is checking out. We can use a `calculateTax` function to figure out the amount of tax due, then store the return value of that function in the variable `taxAmount` to do further calculations: 

```javascript
function calculateTax(cartValue){
  // calculate a flat tax of 7%
  const taxDue = cartValue * (7 / 100);
  return taxDue;
}

function checkout(){
  // Normally, this data would be calculated elsewhere. 
  // We're hard coding it to simplify a bit: 
  cartValue = 45 + 39 + 20 + 20;       // 124 
  // Store the return value of this function:
  const taxAmount = calculateTax(cartValue);
  // Using that return value, we can return the cart total plus the required tax:
  return cartValue + taxAmount;
}

console.log(checkout()); // 132.68
```

The ability to store and use return values allows us to use helper functions to keep our code concise and legible. 'Helper functions' are functions that perform a part of the calculations of another function - `calculateTax()` above is a great example. 

Breaking up a larger function into smaller helper functions can make it much easier to understand what a function is doing. Take the following example: 


```javascript 
function compileAndSend() {
  let date = new Date();
  let sales = getSalesData(date);
  let labor = getLaborCosts(date);
  let budget = getBudget(date);
  let report = generateReport(date, sales, labor, budget);
  sendReport(report);
}

// Run the function
compileAndSend()

/*--- helper functions ---*/

function getSalesData(forDate) {
  let netSales = getNetSales(forDate);
  let salesTax = computeSalesTax(netSales);
  return {netSales, salesTax};
}

function getLaborCosts(forDate) {
  let staffCosts = getStaffCosts(forDate);
  let mgtCosts = getMgtCosts(forDate);
  return {staffCosts, mgtCosts};
}

function getBudget(forDate) {
  let salesBudget = getSalesBudget(forDate);
  let laborBudget = getLaborBudget(forDate);
  return {salesBudget, laborBudget};
}

function generateReport(forDate, dailySales, dailyLabor, budget) {
  ...
}

function sendReport(report) {
  ... // send the report somewhere
}

// etc.
```

Despite being quite a large function with a lot of code, the helper functions make it fairly easy to follow: 
We're getting the current date, then getting sales data, labor costs, and the budget based on that date. Then, we're compiling that data and sending it off in a report. 

All of this is possible because we're not losing the return values of each of these helper functions. 


## 🧠 You Do: 

Write a function named `computeArea`.

It will have two parameters: `width` & `height`.

It will compute the area of a rectangle (*width* X *height*) and return a string in the following form:

> The area of a rectangle with a width of ___ and a height of ___ is ___ square units
> 

Invoke the function to test it:

```javascript
console.log(computeArea(5, 25))
// output: The area of a rectangle with a width of 5 and a height of 25 is 125 square units
```