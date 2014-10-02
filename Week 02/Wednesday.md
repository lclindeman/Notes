## JavaScript Review

* What is a Statement?
* What is a Variable?
* What is a Function?

```
var name = function (param, param, param ...) {
	statements
};
```

All data types are immutable (unchangeable) except for objects.

## Working with Strings

JavaScript strings are immutable. This means that once created, you can not modify it. You can however create another string based on an operation to the once previously created.

```js
var days = "sunday,monday,tuesday,wednesday,thursday";
```

* `.concat()` - combines the text of two or more strings and returns a new string.
```js
days.concat('friday,saturday');
```
* `.length` - returns the length of the string
```js
days.length;
```
* `.split()` - splits a String object into an array of strings by separating the string into substrings.
```js
days.split(',');
```

## Arrays

Arrays are high-level, list-like objects.

```js
var days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday'];
console.log(days); // Entire Array
console.log(days[1]); // Tuesday
```

* `push()`
* `pop()`
* `slice()`
* `reverse()`

## Conditionals

Truthy vs Falsy

### Falsy

* ""
* 0
* false
* undefined
* null
* NaN

### Truthy

Everything that is not falsy.

### Conditional Operators

* `if`
* `==` vs `===`
* `!=` vs `!==`
* `>` and `<`
* `>=` and `<=`

Do some if statements

```js
if(/* something truthy */){
  // do something
} else {
  //something else
}
```

## Objects

An object is a stand alone entity that can have properties.

In JavaScript almost everything is an object. (other than the primitives)

## Literal syntax
```js
var theObject = {
  someProperty: "cool"
};
```

## Properties
Properties are like variables on objects.

```js
var theObject = {
  someProperty: "cool",
  someOtherProperty: ["hay", "guyz"]
}

// New properties are created automatically when you assign to them
theObject.thirdThing = 123;

// Access properties with the dot (.)
var num = theObject.thirdThing;

// Or with brackets and strings
var cool = thirdThing['cool']
```


## Iteration

### [forEach](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)

```js
[1, 2, 3].forEach(function(num) {
  console.log(num);
});

// => 1
// => 2
// => 3
```

### [map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)

```js
[1, 2, 3].map(function(num) {
  return num * 2;
});

// => [2, 4, 6]
```

### [reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce)

```js
[1, 2, 3].reduce(function(total, current) {
  return total + current;
});
// => 6
```

### [filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)

```js
[1, 2, 3].filter(function(num) {
  return num >= 3;
});
// => [3]
```

### Resources

[More on Truthy vs Falsy](http://www.sitepoint.com/javascript-truthy-falsy/)

