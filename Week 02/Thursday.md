## CSS Transition

```html
.element {
    transition: [transition-property] [transition-duration] [transition-timing-function] [transition-delay];
}
```

```html
div {
  transition: background-color 0.5s ease;
  background-color: red;
}
div:hover {
  background-color: green;
}
```

## Install Party!

For more information, or the commands we did today [go here](http://tiy-atlanta-js.github.io/tools.html).

* Node
* NPM
* Gulp
* Yeoman
* Bower

## Bourbon, Bootstrap, Foundation

Bourbon vs Compass

Is one better? Nope, they are just all different. People will have opinions (like I do) but that doesn't discredit any of them.

## Intro to jQuery

Simple Review of DOM API

```js
document.querySelectorAll('a');

document.getElementByID('container');

document.getElementsByClassName('page_title');
```

> jQuery is a fast, small, and feature-rich JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers. With a combination of versatility and extensibility, jQuery has changed the way that millions of people write JavaScript.


* DOM Traversal and Manipulation
* Event Handling
* Ajax


#### Namespacing

`$` or `jQuery` - `noConflict()`

#### Grabbing elements in the DOM

```html
<div class="box box1"></div>
<div class="box box2"></div>
```

```js
$('.box'); // Grabs both boxes
$('.box1'); // Grabs just the first box
```

#### Chaining

```js
$('.box').html('Hello World').addClass('animated').css('margin-left, 25px');
```

#### Methods for editing attributes & content

* `addClass()`
* `removeClass()`
* `toggleClass()`
* `html()`
* `text()`
* `val()`

#### Event Handling

`el.addEventListener('click', listener);`

In jQuery we can use the [`.on()`](http://api.jquery.com/on/) or break it down to using `.click()`, `.hover()` etc. (See below for more events)

Each of these events takes a callback and provides us access to the element we are working with.

```js
$('.box1').click( function () {
	// Statements go in here
	// Refer to the element we are working with $(this)
	$(this).removeClass('box'); // this removes the class of `box` from the element
});
```

## Resources
- [jQuery Basics](http://jqfundamentals.com/chapter/jquery-basics)
- [jQuery Manipulation](http://api.jquery.com/category/manipulation/)
- [jQuery Attributes](http://api.jquery.com/category/attributes/)
- [jQuery Selectors](http://api.jquery.com/category/selectors/)
- [jQuery Events](http://api.jquery.com/category/events/)
- [CSS Transitions](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Using_CSS_transitions)
- [More CSS Transitions](http://css-tricks.com/almanac/properties/t/transition/)
