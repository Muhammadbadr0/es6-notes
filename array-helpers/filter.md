## filter Helper

### ES5 loop version 

```js
var products = [
  {name: 'cucumber', type: 'vegetable'},
  {name: 'banana', type: 'fruit'},
  {name: 'celery', type: 'vegetable'},
  {name: 'orange', type: 'fruit'},
]
var filteredProducts = [];

for(var i = 0; i < products.length; i++){
  if(products[i].type === 'fruit'){
    filteredProducts.push(products[i])
  }
}
```

### ES6 filter helper version 

```js
var products = [
  {name: 'cucumber', type: 'vegetable'},
  {name: 'banana', type: 'fruit'},
  {name: 'celery', type: 'vegetable'},
  {name: 'orange', type: 'fruit'},
]

var filteredProducts = products.filter(function(product){
  return product.type === 'fruit'
})
```

### More examples 

```js
var products = [
  {name: 'cucumber', type: 'vegetable', quantity: 0, price: 1},
  {name: 'banana', type: 'fruit', quantity: 10, price: 15},
  {name: 'celery', type: 'vegetable', quantity: 30, price: 7},
  {name: 'orange', type: 'fruit', quantity: 3, price: 5},
]
var filteredProducts = products.filter(function(product){
  return product.type === 'vegetable' && product.quantity > 0 && product.price < 10
})
```

```js
var post = {id: 4, title: 'New Post'};

var comments = [
	{postId: 4, content: 'awesome!'},
	{postId: 3, content: 'It was ok'},
	{postId: 4, content: 'neat'}
]

function commentsForPost(post, comment){
	return comments.filter(function(comment){
		return comment.postId === post.id
	})
}

commentsForPost(post, comments)
```

