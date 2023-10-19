# Intro to JavaScript Functions - Level Up - Rest Parameters

![Hero image](./assets/hero-rest-parameters.png)

The [rest parameter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/rest_parameters) syntax allows a function to accept any number of arguments as a named array. The syntax is identical to the [spread operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax). While the spread operator expands an array into its elements, the rest syntax does the opposite, taking multiple arguments and condensing them into a single array.

```javascript
// Each argument is condensed into a single array called scores
function calculateAverage(...scores){
  let total = 0;
  // Loop over the scores array to tally up the total
  scores.forEach(function(score){
    total = total + score;
  });
  // Divide the total by the length of the array to find the average
  return total / scores.length;
}

calculateAverage(1, 2, 3, 4, 5, 6, 7, 8, 9, 10); // returns 5.5
```
