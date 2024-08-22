<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>If Statements</title>
  </head>
  <body>
    <h1>If Statements</h1>

    <script src="script.js"></script>
  </body>
</html>


| Operation | Definition |
| --- | --- |
| &lt; | Less Than |
| &gt; | Greater Than |
| &lt;= | Less Than or Equal to |
| &gt;= | Greater Than or Equal to |
| == | Equal to |
| != | Not Equal to |
| === | Equal to w/ type |
| !== | Not Equal to w/ type |


```js
// If Statement Syntax
if (true) {
  console.log('This is true');
}

if (false) {
  console.log('This is NOT true');
}

// Evaluation expressions
const x = 10;
const y = 5;

if (x >= y) {
  console.log(`${x} is greater than or equal to ${y}`);
}

if (x === y) {
  console.log(`${x} is equal to ${y}`);
} else {
  console.log(`${x} is NOT equal to ${y}`);
}

// Block scope
if (x !== y) {
  const z = 20;
  console.log(`${z} is 20`);
}

console.log(z); // Throw error

// Shorthand If/Else
if (x >= y)
  console.log(`${x} is greater than or equal to ${y}`),
    console.log('This is true');
else console.log('This is false');
