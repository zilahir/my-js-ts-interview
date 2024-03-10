# Intro

## Questions

### Class method vs Arrow function

```typescript
class Example {
  location = "Class",

  arrow = () => {
    console.log("arrow", this)
  },

  method() {
    console.log("method", this)
  }
}

const obj = {
  location: "Object",
  arrow: new Example().arrow,
  method: new Example().method,
}

// what's the location?

obj.arrow();
obj.method();

```

### Hoisting

What will be printed to the console?

```typescript
console.log(a);
let a = a;

console.log(a);
var a = 1;
```

### Floating point arithmetic & Binary representation

What it is?

```typescript
const result = 0.1 + 0.2;
console.log(result);
```

```typescript
const binarySum = (a, b) => {
  const sum = a + b;
  return sum.toString(2);
};

const binaryResult = binarySum(0.1, 0.2);
console.log(binaryResult);
```

### TS Compilation

Which one is faster, and why?

```typescript
type A = B & C;

interface D extends B, C {}
```

### Binding

What will be printed to the console?

```typescript
var x = 20;

const myObj = {
  x: 50,
  foo: function () {
    console.log(this.x);
  },
};

myObj.foo();

const foo = myObj.foo;
foo();
```

### Call Stack

What will be printed to the console?

```typescript
for (var i = 0; i < 5; i++) {
  setTimeout(() => console.log("i = ", i), i * 10);
}
```

### Event Loop & Queue

Put the logs in order.

```typescript
Promise.resolve().then(() => console.log(1));

queueMicrotask(() => console.log(2));

setTimeout(() => consoele.log(3), 0);

console.log(4);

new Promise(() => console.log(5));

(async () => console.log(6))();
```
