# Combine Multiple Arrays Using Spread

Combine Multiple Arrays using ES6 Spread β¬π€©

Instead of using concat() to concatenate arrays, try using the spread syntax to combine multiple arrays into one flattened arrayπ


```javascript
let veggie = ['π', 'π₯'];
let meat = ['π₯'];

// Old Way 
let sandwich = veggie.concat(meat, 'π');
console.log(sandwich); // [ 'π', 'π₯', 'π₯', 'π' ]

// ES6 Way
let sandwich2 = [...veggie, ...meat, 'π'];
console.log(sandwich2); // [ 'π', 'π₯', 'π₯', 'π' ]
```

## Resources

- https://davidwalsh.name/spread-operator
- https://gist.github.com/yesvods/51af798dd1e7058625f4
