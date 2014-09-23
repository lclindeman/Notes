# Monday

### HTML Overview

  * What is HTML
  * Overview of doctype, html, head, body
    * `<!DOCTYPE html>` - HTML5 Doctype
  * HTML Properties
    - `<doctype>`
    - `<html>`
    - `<head>`
    - `<body>`
    - `<p>`
    - `<div>`
    - `<a>`
    - `<h1>`
    - `<img>`
    - `<ul>`
    - `<ol>`
  * Block vs Inline
     * Block
        * If no width is set, will expand naturally to fill its parent container
        * By default, will be placed below previous elements in the markup
        * Examples:  `<p>`, `<div>`, `<ul>`, `<li>`, and `<h1>`.
     * Inline
        * Flows along with text content
        * Examples:  `<a>`, `<span>`, `<img>`


### CSS overview


  * What is CSS?
    * Overview of adding colors, styling fonts, etc.
    * Adding styling with id and class names
  * CSS Properties
	* background
	* color
	* hex vs rgb vs rgba vs hsl
      * HEX is the original, pretty simple and easy to use/remember
      * RGB/RGBA is newer and pretty well known. It supports transparency. Red, Green, Blue, Alpha
      * HSLA is the newest and is not fully supported so you need to be careful. Hue, Saturation, Lightness, Alpha
			* display
	* margin
	* padding
	* height / width
	* `margin: 0 auto` centering

### Links / Resources

* [HLS Color Picker](http://hslpicker.com/)
* [Color Picker](http://colorsnapper.com/)
* [Mozilla Developer Network](https://developer.mozilla.org/en-US/)
* [HEX vs RGBa vs HSLa](http://www.ironion.com/colors-on-the-web-rgb-vs-hex-vs-hsla/)
* [HTML Properties](http://www.htmldog.com/reference/htmltags/)
* [CSS Properties](http://www.htmldog.com/reference/cssproperties/)


___The last two are a little out dates, but still give a good example of the list of elements/properties.___


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
