# every and some helpers 

### ES5 Loop Version

```js
var computers = [
	{name: 'Apple', ram: 240},
	{name: 'Compaq', ram: 4},
	{name: 'Acer', ram: 32}
];

var allComputersCanRunProgram = true;
var onlySomeComputersCanRunProgram = false;

for(var i = 0; i < computers.length; i++){
	var computer = computer[i];

	if(computer.ram < 16){
		allComputersCanRunProgram = false;
	} else {
		onlySomeComputersCanRunProgram = true;
	}
}
```

### ES6 every & some helper Version 

```js
var computers = [
	{name: 'Apple', ram: 240},
	{name: 'Compaq', ram: 4},
	{name: 'Acer', ram: 32}
];

var allComputersCanRunProgram = computers.every(function(computer){
	return computer.ram > 16
})
var onlySomeComputersCanRunProgram = computers.some(function(computer){
	return computer.ram > 16
})
```

### Examples 

```js
var names = ["Alex", "Matthew", "Joe"];

names.every(function(name){
	return name.length > 4;
})
names.some(function(name){
	return name.length > 4;
})
```