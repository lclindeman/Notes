# Tuesday

### Child Selectors

```html
<div class="outer">
	<div class="inner">
		<div class="very-inner"></div>
	</div>
</div>
```

```css
// targets inner, but not very-inner
.outer > div {

}
```

### Descendent Selector

```css
// targets both inner and very-inner
.outer div {

}
```

### Floating

* `float: left;`
* `float: right;`
* `float: none'`

[Clearfix Hack](http://learnlayout.com/clearfix.html)

Other ways to clear your floats?


### Positioning

[CSS Positioning](https://developer.mozilla.org/en-US/docs/Web/CSS/position)

* `position:relative;`
* `position:absolute;`

Introduction of `top`, `right`, `bottom`, `left` and `z-index`

### Links / Resources

[CodePen from Class](http://codepen.io/twhitacre/pen/2e9e33c04209cc3ccdfe5b1b77a8690f/)
[HTML Attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)
[CSS Shorthand Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Shorthand_properties)
[CSS Selectors](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started/Selectors)
[CSS Z-INDEX](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Understanding_z_index/The_stacking_context)
[Learn Layout](http://learnlayout.com/)
