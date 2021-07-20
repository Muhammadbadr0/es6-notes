## forEach Helper

Normally, we would write a `for` loop to iterate over a number of elements inside an array to work on them. This works, however, It's a complex and more error-prone process.

```js
var colors = ["red", "blue", "green"];

for(var i = 0; i < colors.length; i++){
	console.log(colors[i]);
}
```

In ES6, Arrays have a `forEach` method, which does the same in a less error-prone way, `forEach` accepts an anonymous function (iterator) as an argument, which gets called one time for each element in the array.

```js
colors.forEach(function(color){
	console.log(color);
})
```

### Examples 

```js
var numbers = [1, 2, 3, 4, 5];

var sum = 0;

numbers.forEach(function(number){
	sum += number
})

console.log(sum)
```

```js
const words = ['hello', 'bird', 'table', 'football', 'pipe', 'code'];

const capWords = words.forEach(capitalize);
 
function capitalize(word, index, arr) {
  arr[index] = word[0].toUpperCase() + word.substring(1);
}
console.log(words);
```
