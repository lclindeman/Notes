## It's RWD Day!

* Everything is based off Sam Kapila's [RWD Handy Checklist](http://samkap.github.io/projects/tiy-rwd/)
* Example from class today - [Right Here](https://gist.github.com/twhitacre/fcdd910824ca9ba407df)

#### HTML Setup

1. Add a `meta` `viewport` in your head
2. Add a link to your stylesheet like usual
3. Create a container element... will be useful later.
	* Generally, I set a `max-width` on it.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link href="style.css" type="text/css" rel="stylesheet">

<div class="container"></div>
```

#### Flexible Layout

* Keep anything `left` or `right` or or `width` related in percents (except max-widths)
* Use pixels or ems for anything `top`, `bottom`, or `height` related.
* Also, as a general rule, all `width` should be in percentages except max-widths (most cases)

#### Mobile First

* Use media queries from smallest to largest (mobile-first approach)
* You also begin with a global CSS that does not need to be in a media query.
* `min-width` vs `max-width`

```css
@media (min-width: 1200px) {

}
```

```css
/*Default styles*/
.related-products li {
  float: left;
  width: 50%;
}

/*Display 3 per row for medium displays (like mobile phones in landscape or smaller tablets)*/
@media screen and (min-width: 28.75em) {
  .related-products li {
    width: 33.3333333%;
  }
}
/*Display 6 to a row for large displays (like medium tablets and up) */
@media screen and min-width: 40.5em) {
  .related-products li {
    width: 16.6666667%;
  }
}
```

#### Flexible Type

```css
body {
		font-face: "Adobe Caslon Pro", Georgia, serif;
		body { font-size: 62.5%; }
}
```

#### Flexible Images (& Videos)

Usually applied globaly

```css
img {max-width:100;}
```

[FitVids](http://fitvidsjs.com/)


#### [Retina](http://briancray.com/posts/detect-retina-displays-with-javascript)

```js
window.devicePixelRatio
```


## Resources

* [The Article that Started it All](http://alistapart.com/article/responsive-web-design)
* [Mobile First](http://www.html5rocks.com/en/mobile/responsivedesign/)
* [Mobile First (another one)](http://zurb.com/word/mobile-first)
* [Nice Examples](http://mediaqueri.es/)
* [MDN Media Queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)
