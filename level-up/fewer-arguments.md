# Fewer Arguments Than Parameters Defined

JavaScript is very flexible and won't complain when the number of arguments is not the same as the number of parameters defined.

If fewer arguments are passed than parameters defined, then the parameter variables without a matching argument would be set to undefined.

```javascript
function add(a, b, c) {
  console.log(a, b, c); // 5, 2, undefined
}

add(5, 2);

```

Unlike some other programming languages, JavaScript won't complain if fewer (or extra) arguments are passed to a function. However, a function that depends on certain arguments to do its job might throw an error or return an unexpected result if it doesn't receive the arguments expected.