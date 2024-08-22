<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Freezing & Sealing Properties</title>
  </head>
  <body>
    <h1>Freezing & Sealing Properties</h1>

    <script src="script.js"></script>
  </body>
</html>

```js
// Sealing - Prevents properties from being added or removed. Can still be changed.

// Freezing - Prevents properties from being added, removed or changed

const rectObj = {
  name: 'Rectangle 1',
  width: 10,
  height: 10,
};

Object.seal(rectObj);

let descriptors = Object.getOwnPropertyDescriptors(rectObj);
// console.log(descriptors);

//  Can not add and remove properties
rectObj.color = 'red';
delete rectObj.name;

// Can change values
rectObj.width = 20;

// console.log(rectObj);

const circleObj = {
  name: 'Circle 1',
  radius: 30,
};

Object.freeze(circleObj);

descriptors = Object.getOwnPropertyDescriptors(circleObj);

// Can not add, remove or modify
circleObj.color = 'blue';
delete circleObj.name;
circleObj.name = 'New Name';

console.log(descriptors);

// If an object is frozen, it is also sealed
console.log('rectObj is sealed?', Object.isSealed(rectObj));
console.log('rectObj is frozen?', Object.isFrozen(rectObj));
console.log('circleObj is sealed?', Object.isSealed(circleObj));
console.log('circleObj is frozen?', Object.isSealed(circleObj));
