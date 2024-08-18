<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="script.js" defer></script>
    <title>Queues</title>
  </head>
  <body>
    <h1>Queues</h1>
  </body>
</html>

```js
class Queue {
  constructor() {
    this._items = [];
    this._count = 0;
    this._front = 0;
  }

  enqueue(item) {
    this._items[this._count] = item;
    this._count++;
  }

  dequeue() {
    if (this.isEmpty()) {
      return undefined;
    }

    const item = this._items[this._front];
    for (let i = this._front; i < this._count - 1; i++) {
      this._items[i] = this._items[i + 1];
    }
    this._count--;
    this._items.length = this._count;
    return item;
  }

  peek() {
    if (this.isEmpty()) {
      return 'No items in the queue';
    }

    return this._items[this._front];
  }

  length() {
    return this._count - this._front;
  }

  isEmpty() {
    return this._count === 0;
  }
}

const q = new Queue();

q.enqueue('Item 1');
q.enqueue('Item 2');
q.enqueue('Item 3');

q.dequeue();
q.dequeue();

console.log('Front Item: ', q.peek());
console.log('Queue Length: ', q.length());
