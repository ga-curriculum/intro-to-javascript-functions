<h1>
  <span class="headline">Intro to JavaScript Functions</span>
  <span class="subhead">Concepts</span>
</h1>

**Learning Objective:** By the end of this lesson, the learner will be able to explain how JavaScript functions can simplify complex tasks and promote code reusability.

## What is a function? 

A *function* is a reusable block of code written to perform a single purpose. With a function, you can store code that can be used conveniently as many times as you wish without having to rewrite the code each time. As a result, functions are one of the fundamental building blocks of JavaScript, and you'll find and use them everywhere. 

![A function, taking in a block as input and outputting a star](./assets/function-input-output.png)

Functions optionally take in data as input and return a single piece of data (including complex data such as objects or other functions).

> 📚 A *function* is a block of code that can be called as needed and is designed to perform a specific task. A function may accept input and can return a result after completing its task.

## Why are functions essential in programming?

### Tackle complexity

We typically tackle a complex task by breaking it into smaller tasks or steps - when we're programming, we want to do the same! Functions allow us to break up programs into more manageable blocks of code.

### Code reuse

Functions help us reuse code by allowing us to run the same set of instructions multiple times. For example, a `renderBoard` function might be called every time the data in a board changes.

This helps us avoid repeating the same code in many places — a principle often called **"Don't Repeat Yourself"** (or DRY). Writing code this way makes it easier to read, fix, and update later.

### Documentation & debugging 

Naming functions appropriately, for example a name like `renderBoard` helps document what that function's job is (to show the user the current game board).Organizing code into functions also makes it easier to find and fix code that's not working as expected, a process known as debugging.
