# 2 Ways to Repeat Strings

2 ways to repeat strings in JavaScript π Iβve always used βArray.fillβ to do any repetitions. βrepeatβ is a recent discovery π€©

```javascript
const canada = 'π¨π¦'

// Repeat method
canada.repeat(3)

// Fill method
Array(3).fill(canada).join('')

// result
'π¨π¦π¨π¦π¨π¦'
```

## How `repeat` works

The repeat method simply repeats your string. It returns a new string that concatentates the specified number of copies you indicated.

```javascript
'π¨π¦'.repeat(3); // 'π¨π¦π¨π¦π¨π¦'

'Hey'.repeat(2); // 'HeyHeyHey'

'Blank'.repeat(0); // ''
```

## How `fill` works

```javascript

// Step 1: Create an new array with 3 empty items
Array(3)

  // Step 2: Fill each empty slot with 'π¨π¦'
  .fill('π¨π¦')
  
  // Step 3: Join all the elements into a string
  .join('');
```

## Community Examples

### Using `for` loop

A classic example of repeating strings using the `for` loop π

```javascript
const canada = 'π¨π¦'
const arr = [];

for(let i = 1; i <= 3; i++) {
  arr.push(canada);
}

arr.join(''); // 'π¨π¦π¨π¦π¨π¦'
```

_Thanks: Alen H._

### Using `join` only

A even shorter shortcut to repeat string using just the `join` method. Cool βοΈ

```javascript
Array(4).join('π¨π¦')

// returns 'π¨π¦π¨π¦π¨π¦'
```

_Thanks: Diogo D._

### Using `Array.from`

This is an interesting example

```javascript
Array.from({length: 3}, () => 'π¨π¦').join('');

// returns 'π¨π¦π¨π¦π¨π¦'
```

_Thanks: [@oliverturner](https://twitter.com/oliverturner/status/1013527580987797504)_

### βοΈ How that works?

Let me break down Oliver's example and explain it a bit more.

**1.**

The `length` property of the `from()` method is 1. So we set the length property to 3, which initializes the array with 3 corresponding `undefined` in each position.

```javascript
Array.from({length: 3});

// returns [undefined, undefined, undefined]
```

**2.**

Now we utilize the 2nd parameter, which is a map function that will make a call on every element of the array. Here we are replacing all the `undefined` with 'π¨π¦'. Notice I've split this into two lines with `{}`, hence I need to use a `return`.

```javascript
Array.from({length: 3}, () => {
  return 'π¨π¦'
});

// returns ['π¨π¦', 'π¨π¦', 'π¨π¦']
```

**3.**

Finally we call `join()` to combine all the elements in the array into a string.

```javascript
Array.from({length: 3}, () => {
  return 'π¨π¦'
}).join('');

// returns 'π¨π¦π¨π¦π¨π¦'
```

## Resources

- [MDN Web Docs - fill()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/fill)
- [MDN Web Docs - repeat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/repeat)
