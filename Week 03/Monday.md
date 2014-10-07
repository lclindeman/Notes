## Iterations Review

### Start with an array

```js
var names = ['tim', 'sean', 'greg', 'bill', 'julie', 'sam', 'linda'];
```

Each one of the following iterations will spit out each name as it loops through them.

### forEach

```js
names.forEach( function (name) {
	console.log(name);
});
```

### for ... in

Iterates over the properties of an object, in arbitrary order.

For each property, statements can be executed.

```js
for (var i in names) {
	console.log(names[i]);
}
```

### for loop

Creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons, followed by a statement executed in the loop.

```js
for (var i = 0; i < names.length; i++) {
	console.log(names[i]);
}
```


### while loop

Creates a loop that executes a specified statement as long as the test condition evaluates to truthy. The condition is evaluated before executing the statement.

```js
var x = 0;
while ( x < names.length ) {
	console.log(names[x]);
	i++;
}
```

## jQuery Review

Read  about '.on' & delegate events [here](http://api.jquery.com/on/)


## Resources

* [You Might Not Need jQuery](http://youmightnotneedjquery.com/)
* [Zepto - Alternative to jQuery](http://zeptojs.com/)
* [Backup Your .dot Files](http://dotfiles.github.io/) - just a good practice

## Learn More

To continue learning, I suggest building your own version of some of the built in array functions.

For instance, build one for `map()`, `reduce()` and `filter()`. You can use a `forEach()` or a simple `for` or `for in` loop. This will help you understand what is going on behind the scenes.
