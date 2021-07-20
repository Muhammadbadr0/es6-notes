# reducer Helper 

### ES5 Loop Version 

```js
var numbers = [10, 20, 30];
var sum = 0;

for(var i = 0; i < numbers.length; i++){
	sum += numbers[i]
}
```

### ES6 reducer helper Version 

```js
var numbers = [10, 20, 30];

numbers.reduce(function(sum, num){
	return sum + num
}, 0)
```

### Examples 

```js
var primaryColor = [
	{color: 'red'},
	{color: 'yellow'},
	{color: 'blue'}
];

primaryColor.reduce(function(prev, prime){
	prev.push(prime.color);

	return prev;
}, [])
```

```js
function balancedParans(string){
	return !string.split("").reduce(function(prev, char){
		if(prev < 0) { return prev};
		if(char === "(") {return ++prev}
		if(char === ")") { return --prev}
		return prev
	}, 0)
}

balancedParans("(())")
```