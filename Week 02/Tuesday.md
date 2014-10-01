# Welcome to JavaScript

> "Learn you a JavaScript, for great good"

JavaScript is an object-oriented computer programming language commonly used to create interactive effects within web browsers.

[The Origin of JavaScript (JS Jabber Podcast)](http://javascriptjabber.com/124-jsj-the-origin-of-javascript-with-brendan-eich/)

## Variable
Label for a value.

### Declare a variable
```js
var name;
```

### Assign a value to a variable

```js
name = 'Tim';
```

### Shorthand

Declare and assign:
```js
var name = 'Tim';
```

## DOM

The dom is the Document Object Model and it is a way for us to interact with our HTML page.

Take this HTML for example

```html
<div class="container">
	<input type="text" id="username" />
</div>
```
If I wanted to get the value of my "username" input I would do the following:

```js
// Use the document object to get a specific input
var userField = document.getElementById('username');

// Use the value property of my username object to get the text in that input
var username = userField.value;
```

## [Types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)

There are two main types in JS, Primitives & Objects.

> Primitives are not objects and do not have any methods. In other words, you can't break a primitive down any further.

* String
* Number
* Boolean
* Undefined
* Null

> Objects are data structures and can be broken down.

## Resources

* [The Ultimate Guide to JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
