<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Math Object</title>
  </head>
  <body>
    <h1>Math Object</h1>

    <script src="script.js"></script>
  </body>
</html>

```js
let x;

// Square root
x = Math.sqrt(9);

// Absolute value
x = Math.abs(-5);

// Round
x = Math.round(4.2);

// Round up
x = Math.ceil(4.2);

// Round down
x = Math.floor(4.9);

// Exponent
x = Math.pow(2, 3);

// Minimum number
x = Math.min(4, 5, 3);

// Maximum number
x = Math.max(4, 5, 3);

// Get a random number/decimal between 0 and 1
x = Math.random();

// Get a random number between 1 and 100
x = Math.floor(Math.random() * 100 + 1);

console.log(x);
