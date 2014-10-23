## Ternary

```js
if (condition){
  result = 'something';
} else {
  result = 'something else';
}
```

```js
result = (condition) ? 'something' : 'something else';
```


## JSHint

> JSHint is a tool that helps to detect errors and potential problems in your JavaScript code.

```js
// Install
npm install -g jshint

// Basic Usage on single file
jshint main.js
```

Read more [here](http://jshint.com)

## IIFE

> Immediately Invoked Function Expression

> An IIFE protects a module’s scope from the environment in which it is placed.

```js
(function(){
  // my special code
}());
```

> By wrapping the anonymous function inside of parentheses, the JavaScript parser knows to treat the anonymous function as a function expression instead of a function declaration. A function expression can be called (invoked) immediately by using a set of parentheses, but a function declaration cannot be.


* Function Expression - `var test = function() {};`
* Function Declaration - `function test() {};`

#### Benefits

* Reduces the objects added to the window object
* Reduce scope lookups

  ```js
  (function(window, document, $){
    // my special code
  }(window, document, window.jQuery));
  ```

  > Note: JavaScript first looks for a property in the local scope, and then it goes all the way up the chain, last stopping at the global scope. Being able to place global objects in the local scope provides faster internal lookup speeds and performance.


## Scope

> Variable Access

_What variables do I currently have access to?_


## Context or `this`

Examples of `this`

```js
var anyObj = {
  me: function () {
    console.log(this);
  }
};

anyObj.me(); // anyObj

// call, apply
anyObj.me.call(window); //  window

// bind - returns a bound function
var newObj = anyObj.me.bind(window);
newObj(); // window
anyObj.me(); // anyObj
```


#### `this` in jQuery

> Set up a page with multiple elements and click on different ones

```js
// Pass `this` around
$('h1').on('click', function () {
  var newTitle = 'My New title';
  var self = this;
 $('elem').fadeOut(300, function () {
   // what is this?
   self;
 });
});
```

## Resources

* [What is the Event Loop](http://www.youtube.com/watch?v=8aGhZQkoFbQ)
* [Loupe](http://latentflip.com/loupe)
* [JSHint](http://www.jshint.com/)