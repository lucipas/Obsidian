<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Constructor Functions</title>
  </head>
  <body>
    <h1>Constructor Functions</h1>

    <script src="script.js"></script>
  </body>
</html>

```js
// Constructor Function
function Rectangle(name, width, height) {
  this.name = name;
  this.width = width;
  this.height = height;
  this.area = function () {
    return this.height * this.width;
  };
}

// We can create as many instances of our Rectangle objects as we want using the `new` keyword
const rect1 = new Rectangle('Rectangle 1', 10, 10);
console.log(rect1.name);
console.log(rect1.area());

const rect2 = new Rectangle('Rectangle 2', 20, 10);
const rect3 = new Rectangle('Rectangle 3', 30, 30);

console.log(rect2.name, rect3.name);
console.log(rect2.area(), rect3.area());

// When we use the `new` keyword, 4 things happen:
// 1. A new empty object is created.
// 2. The constructor function is called with the arguments that we passed in.
// 3. The `this` keyword is set to the new empty object.
// 4. The new object is returned from the constructor function.

// We can access the constructor function with the `constructor` property
console.log(rect1.constructor);

// Check to see if an object is an instance of a constructor
console.log(rect2 instanceof Rectangle);
