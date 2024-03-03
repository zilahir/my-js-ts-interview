# Intro

## Questions

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
