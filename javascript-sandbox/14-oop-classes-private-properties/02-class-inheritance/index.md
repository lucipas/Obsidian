<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Class Inheritance</title>
  </head>
  <body>
    <h1>Class Inheritance</h1>

    <script src="script.js"></script>
  </body>
</html>

```js
// Parent class
class Shape {
  constructor(name) {
    this.name = name;
  }

  logName() {
    console.log('Shape Name: ' + this.name);
  }
}

// Rectangle - Sub class
class Rectangle extends Shape {
  constructor(name, width, height) {
    super(name);

    this.width = width;
    this.height = height;
  }
}

// Circle - Sub class
class Circle extends Shape {
  constructor(name, radius) {
    super(name);

    this.radius = radius;
  }

  // We can override the Shape logName() (polymorphism)
  logName() {
    console.log('Circle Name: ' + this.name);
  }
}

const rect = new Rectangle('Rect 1', 20, 20);
console.log(rect);
rect.logName();

const cir = new Circle('Cir 1', 30);
cir.logName();

// rect is an instance of both Rectangle and Shape
console.log(rect instanceof Rectangle);
console.log(rect instanceof Shape);
