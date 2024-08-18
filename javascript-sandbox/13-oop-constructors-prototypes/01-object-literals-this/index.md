<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Object Literal & this Keyword</title>
  </head>
  <body>
    <h1>Object Literal & this Keyword</h1>

    <script src="script.js"></script>
  </body>
</html>

```js
const rectangle = {
  name: 'Rectangle 1',
  width: 20,
  height: 10,
  // We can add methods to an object and use this keyword to access the properties of the object
  area: function () {
    return this.width * this.height;
  },
};

// Object literals are great for creating objects that only need one instance. If we needed two Rectangles, we would have to create two objects

const rectangle2 = {
  name: 'Rectangle 2',
  width: 30,
  height: 20,
  area: function () {
    return this.width * this.height;
  },
};

console.log(rectangle.area());
console.log(rectangle2.area());
