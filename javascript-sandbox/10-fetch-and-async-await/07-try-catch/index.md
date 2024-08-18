<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Try... Catch</title>
  </head>
  <body>
    <h1>Try... Catch</h1>

    <script src="./script.js"></script>
  </body>
</html>

```js
// try {
//   console.log(x);
// } catch (error) {
//   console.log('Error: ' + error);
// }

function double(number) {
  if (isNaN(number)) {
    throw new Error(number + ' is not a number');
  }

  return number * 2;
}

try {
  const y = double('hello');
  console.log(y);
} catch (error) {
  console.log(error);
}
