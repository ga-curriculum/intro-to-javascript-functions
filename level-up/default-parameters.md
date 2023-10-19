# Intro to JavaScript Functions - Level Up - Default Parameters

![Hero image](./assets/hero-default-parameters.png)

What if your function ***requires*** certain arguments, and you want to provide a default value for the parameter if an argument is not supplied when the function is invoked?

JavaScript has the option to specify *default parameters*. By specifying a default, `name` will always equal `'friend'` unless an argument is supplied! This overrides the default behavior of `name` being `undefined` unless an argument is passed.

```javascript
const sayHi = (name = 'friend') => {
  console.log(`Hi ${name}!`);
}
```

```javascript
sayHi();
// Prints: 'Hi friend!'
```

```javascript
sayHi('Joe');
// Prints: 'Hi Joe!'
```

Any expression can be provided as a default, including objects, functions, etc.
