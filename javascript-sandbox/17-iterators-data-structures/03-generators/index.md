<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="script.js" defer></script>
    <title>Generators</title>
  </head>
  <body>
    <h1>Generators</h1>
  </body>
</html>

```js
function* createTeamIterator(teams) {
  for (let i = 0; i < teams.length; i++) {
    yield teams[i];
  }
}

const teams = ['Red Sox', 'Yankees', 'Astros', 'Dodgers'];

const iterator = createTeamIterator(teams);

console.log(iterator.next().value); // Red Sox
console.log(iterator.next().value); // Yankees
console.log(iterator.next().value); // Astros
console.log(iterator.next().value); // Dodgers
console.log(iterator.next().done); // true

// Use with for... of
for (const team of createTeamIterator(teams)) {
  console.log(team);
}

// Use with spread operator
console.log([...createTeamIterator(teams)]);

// Use with destructuring
const [first, second, third] = createTeamIterator(teams);
console.log(first, second, third);
