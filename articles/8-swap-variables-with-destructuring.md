# Swapping Variables With Destructuring

ES6 Destructuring to the rescue π

Easily swap two variables using ES6 destructing. Itβs a great way to fix #Oscars Best Picture mix-ups π


```javascript
let oscar = 'La La Land';
let nominee = 'Moonlight';

[oscar, nominee] = [nominee, oscar];

console.log(oscar) // Moonlight
console.log(nominee) // La La Land
```
