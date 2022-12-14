# Extracting Arguments using Array Destructure

Happy Fatherβs Day!

Array Destructuring is terrific at extracting value from your arguments. So the next time you see the array bracket notation, just swap them out and use array destructuring syntax instead π


```javascript
function sendLove(...args) {

  // β Old way
  const hug = args[0];
  const gift = args[1];

  // β Better way using Array Destructure
  const [icon, gift] = args;
}

sendLove('π€', 'π')
```

The first thing weβre doing is spreading our arguments, so you can get an array. Next weβre assigning them to our variables using array destructuring.

```javascript
// Step 1:
(...args)
args // [ 'π€', 'π' ]


// Step 2:
const [icon, gift] = args;

icon // 'π€'
gift // 'π'
```

## Understanding the `arguments` Object

There's been some confusion on the syntax. I think it's because of the arguments objects. So I'm going to try to explain it. In every function, there is a built in `arguments` object. The `arguments` object is an Array-like object that corresponds to the arguments passed into a function.

```javascript
function sendLove() {

  console.log(arguments); // { 0: 'π€', 1: 'π' }
}

sendLove('π€', 'π')
```

As you can see the `arguments` is not an array. That's why in "Step 1", I'm using the `...` spread syntax to convert it to a real array. So this is essentially what I'm doing:

```javascript
function sendLove(...args) {
}

// Same as

function sendLove() {
  var args = [...arguments];
  console.log(args) // [ 'π€', 'π' ]
}
```

That's why I can name it whatever I want:

```javascript
function sendLove(...hello) {
  console.log(hello); // [ 'π€', 'π' ]
}
```

Read more about the `arguments` object here:
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/arguments


## Resources

- https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment#Array_destructuring
- http://www.deadcoderising.com/2017-03-28-es6-destructuring-an-elegant-way-of-extracting-data-from-arrays-and-objects-in-javascript/
- https://gist.github.com/mikaelbr/9900818
- https://dev.to/sarah_chima/destructuring-assignment---arrays-16f
