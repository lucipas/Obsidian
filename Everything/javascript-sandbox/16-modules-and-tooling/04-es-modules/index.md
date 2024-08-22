<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="app.js" type="module" defer></script>
    <title>ES Modules</title>
  </head>
  <body>
    <h1>ES Modules</h1>
  </body>
</html>

```js
import { capitalizeWords, makeMoney } from './modules/utils.js';
import Person from './modules/Person.js';

console.log(capitalizeWords('hello world'));
console.log(makeMoney(100));

const person = new Person('Mark', 29);
person.greet();
