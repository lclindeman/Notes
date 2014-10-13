## Homework Review

How to break down a timestamp:

```js
var ts = '2014-08-05T01:55:23Z'
var date = new Date(ts);
var months = ['Jan', 'Feb', 'March', 'April', 'May', 'June', 'July', 'Aug', 'Sept', 'Oct', 'Nov', 'Dec'];

console.log( "Updated on " + months[date.getMonth()] + ", " + date.getDay() );
```

> To get the pretty dates "4 hours ago..." you can use [moment.js](http://momentjs.com/)


## Tools Review

* Node
* NPM
* Yeoman
* Gulp
* Bower

## Syntax Review (HTML/CSS)

#### HTML

```html
<!--  1    2       3        4 -->
    <div class="myClass"></div>
```
1. Element Name
2. Attribute Name - (Properties in DOM)
3. Attribute Value
4. Closer


- Attributes are defined by HTML. Properties are defined by DOM.
- Some HTML attributes have 1:1 mapping onto properties. id is one example of such.

#### CSS

```css
div.myClass { /* 1 */
	/* 2 */
  border-color: red; /* 3 : 4 */
}

::before { } /* 5  */
:hover { } /* 6  */
```
1. A Selector
2. Rule
3. Property
4. Value
5. Pseudoelement
6. Pseudoclass

## JavaScript Review

* Function
* Variable
* Paramaters
* Callback
* Object
* Property Accessor (Method / Function)

```js
var person = {
	name: 'Tim',
	greeting: function () {
		alert('Hello there!');
	}
};
```

* `person` is an variable set to an object
* `name` is a property of the `person` object
* `greeting` is a function, but also a method of `person`
* `alert(...)` is a statement inside of our `greeting` method


## Github Review


Review on Branching

* Fetching, Merging
* `git pull` is just `git fetch` and `git merge` in one command. It pulls in the history from the remote, and then merges it into HEAD.

* Forking & Pull Requests
	* Click the 'Fork' Button
	* Clone the fork
	* Do your work
	* Commit & Push
	* Create a Pull Request
