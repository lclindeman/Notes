## Getting the Truth Out of Your data

* See Example [Here](https://gist.github.com/twhitacre/efaacf48f5f3fe2e9fd9)

## Intro to Handlebars

#### In the Browser

> Basic Example

```html
<script type="text/x-handlebars-template" id="book">
  I'm currently reading {{ book }} by {{ author }}
</script>
```

```js
var data = {
  book: 'Moby Dick',
  author: 'Herman Melville'
};

// Grab the template
var source = $('#book').html();

// Compile the Template (creates the function)
var template = Handlebars.compile(source);

// Send that data in
$('.book').html(template(data));
```

> Simple Iterations

```js
var data = {
  books : [
    { book: 'Moby Dick', author: 'Herman Melville' },
    { book: 'Great Expectations', author: 'Charles Dickens'},
    { book: 'Where the Red Fern Grows', author: 'Wilson Rawls'}
  ]
};

var source = $('#books').html();
var template = Handlebars.compile(source);
$('.books').html(template(data));
```

```html
<script id="books" type="text/x-handlebars-template">
  {{#each books }}
    <li>{{ book }} by {{ author }}</li>
  {{/each}}
</script>
```

> Simple Paths

```js
var data = {
  books : [
    { book: 'Moby Dick', author: { name: 'Herman Melville', life: '1819 - 1891' }},
    { book: 'Great Expectations', author: { name: 'Charles Dickens' life: '1812 - 1870' }},
    { book: 'Where the Red Fern Grows', author: { name: 'Wilson Rawls', life: '1913 - 1984' }}
  ]
};
```
``` html
<script id="books" type="text/x-handlebars-template">
  {{#each books }}
    <li>{{ book }} by {{ author.name }} <small>{{ author.life }}</small></li>
  {{/each}}
</script>
```

#### Pre Compiled

```ssh
npm install -g handlebars
```

1. Create a `templates` folder or something
2. Create any `name.handlebars` files you want
3. Run `handlebars <input> -f <output>` from terminal (can use whole directory)
  * Output needs to be a `js` file, usually `/scripts/templates.js`
4. Instead of `Handlebars.compile(source);`, use `Handlebars.templates['books'];` and the key will be the file name


## Intro to JavaScript Testing

* [Writing Testable JavaScript Article](http://alistapart.com/article/writing-testable-javascript)
* [Writing Testable JavaScript Video](http://www.youtube.com/watch?v=OzjogCFO4Zo)