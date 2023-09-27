# Intro to JavaScript Functions - Level Up - Nesting Functions

![Hero image](./assets/hero.png)

We can define functions within functions!

Why would we want to do this? An outer function may need a helper function relevant only to a given function. It would be good programming practice to hide that function from the rest of the program by nesting it within the function that needs it.

For example (no need to execute this):

```javascript
const title = 'This is the title of my cool book';

const toTitleCase = (string) =>{
  const capitalize = (word) => {
    return word.slice(0,1).toUpperCase() + word.slice(1);
  }

  let strArr = string.split(' ');
  strArr.forEach((el, i) => strArr[i] = capitalize(el));
  return strArr.join(' ');
}

toTitleCase(title); // This Is The Title Of My Cool Book
```
