## map Helper

### ES5 loop version
```js
var numbers = [1, 2, 3];
var doubledNumers = [];

for(var i = 0; i < numbers.length; i++){
  doubledNumers.push(numbers[i] * 2)
}
```

### ES6 map

```js
var numbers = [1, 2, 3];
var doubledNumers = [];

var doubled = numbers.map(function(number){
  return number * 2
})
```

### More Examples

```js
var cars = [
  {model: 'Buick', price: 'cheap'},
  {model: 'Camaro', price: 'expensive'}
]

var prices = cars.map(function(car){
  return car.price
})
```