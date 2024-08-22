<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Execution Context</title>
  </head>
  <body>
    <h1>Execution Context</h1>

    <script src="script.js"></script>
  </body>
</html>

```js
//  Go to 'sources' tab and add a breakpoint at the first line and step through to see the execution phase in action
const x = 100;
const y = 50;

function getSum(n1, n2) {
  const sum = n1 + n2;
  return sum;
}

const sum1 = getSum(x, y);
const sum2 = getSum(10, 5);

console.log(sum1, sum2);
