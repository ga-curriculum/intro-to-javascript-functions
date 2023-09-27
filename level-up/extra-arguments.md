# Intro to JavaScript Functions - Level Up - More Arguments than Parameters

![Hero image](./assets/hero.png)

Let's pretend you need to write a function that accepts an unknown number of arguments. For example, let's say we would like to provide any number of "time" arguments to a getPointsScored function and return a total number of points scored.

Here's how we could write `getPointsScored()` to accept any number of individual "time" arguments:

```javascript
// using rest parameter syntax to condense any number of arguments into a single array
const getPointsScored = (...times) => {
  // times will be an array holding the args
  let totalPoints = 0;
  times.forEach(function(time) {
    if (time < 30) {
      totalPoints += 100;
    } else if (time < 60) {
      totalPoints += 75;
    } else {
      totalPoints += 25;
    }
  });
  return totalPoints;
}
	
const points = getPointsScored(16, 99, 32, 60);
```
