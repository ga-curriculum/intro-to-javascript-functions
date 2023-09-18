# Intro to JavaScript Functions - Level Up

![Hero image](./assets/hero.png)

## Immediately Invoked Function Expressions (IIFE)

One way we can prevent our code from leaking into the global scope is by wrapping it with a construct known as an _Immediately Invoked Function Expression_, or “IIFE” (pronounced “iffy”). It looks like this:

```javascript
(function() {
  'use strict';

  // your code here...
	
})()
```

❓ Why does this construct virtually prevent variables and functions from being created in the global scope?