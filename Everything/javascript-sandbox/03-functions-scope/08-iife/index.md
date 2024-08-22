<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>IIFE (Immediately Invoked Function Expressions)</title>
  </head>
  <body>
    <h1>IIFE (Immediately Invoked Function Expressions)</h1>
    <script src="otherscript.js"></script>
    <script src="script.js"></script>
  </body>
</html>

Other Script
```js
const user = 'Brad';
console.log(user);
```

```js
// IFFE Syntax (Has it's own scope and runs right away)
(function () {
  const user = 'John';
  console.log(user);
  const hello = () => console.log('Hello from the IIFE');
  hello();
})();

// Params
(function (name) {
  console.log('Hello ' + name);
})('Shawn');

// Named IIFE (Can only be called recursively)
(function hello() {
  console.log('Hello');
})();
```
