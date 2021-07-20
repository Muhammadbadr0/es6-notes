## find Helper 

### ES5 Loop Version 

```js
var users = [
	{name: 'Jill'},
	{name: 'Alex'},
	{name: 'Bill'}
]

var user;

for(var i = 0; i < users.length; i++){
	if(users[i].name === 'Alex'){
		user = users[i]
		break;
	}
}
```

### ES6 find Helper

```js
var users = [
	{name: 'Jill'},
	{name: 'Alex'},
	{name: 'Bill'}
]

const user = users.find(function(user){
	return user.name === 'Alex';
})
```

### Example

```js
function Car(model){
	this.model = model;
}

var cars = [
	new Car('Buick'),
	new Car('Camaro'),
	new Car('Focus')
];

const car = cars.find(function(car){
	return car.model === 'Focus';
})
```

```js
var posts = [
	{id: 1, title: 'New Post'},
	{id: 2, title: 'old post'}
];

var comments = [
	{postId: 1, content: 'awesome!'},
	{postId: 2, content: 'It was ok'},
	{postId: 2, content: 'neat'}
]

function commentsForPost(posts, comment){
	return posts.find(function(post){
		return post.id === comment.psotId
	})
}

commentsForPost(posts, comments)
```