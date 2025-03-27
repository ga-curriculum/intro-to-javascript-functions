<h1>
  <span class="headline">Intro to JavaScript Functions</span>
  <span class="subhead">Immediately Invoked Function Expressions IIFEs</span>
</h1>

**Learning Objective:** Understand how to use Immediately Invoked Function Expressions (IIFEs) to encapsulate variables and prevent them from entering the global scope.

One way to stop our code from affecting the global scope is by using something called an **Immediately Invoked Function Expression**, or **IIFE** (pronounced "iffy"). This is a special kind of function that runs as soon as it is defined.

Here’s what it looks like:

```javascript
(() => {
  'use strict';

  // your code here
})();
```

The function is wrapped in parentheses to turn it into a complete expression. This is called a [grouping operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Grouping).

After that, the final `()` at the end immediately calls the function. This means the code inside the function runs right away, without waiting for us to call it later.
