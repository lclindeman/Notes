## More Underscore

* Template Review

> This is from the animals.js we created yesterday in class

```js
var string_of_html = $('#animal_template').html();
var rendered_function = _.template(string_of_html);
var final_rendered_html;

$('.hero-unit ul').append(rendered_function(animals));
```

```html
<% _.each(animals, function (a) { %>
  <li>
    <% if (a.name === 'Whale') { %>
    I don't like whales!
    <% } else { %>
    Hi, I am an <%= a.name %> and I live in <%= a.location %>.
    <% } %>
  </li>
<% }); %>
```

## Ajax & $.json()

* $.ajax()
* $.json()
* .done()

## Ajax

```js
$.ajax({
  url: 'https://api.github.com/users/twhitacre',
  dataType: 'json'
});
```

## Get JSON

```js
$.getJSON( 'https://api.github.com/users/twhitacre' );
```

## Done

```js
$.getJSON( 'https://api.github.com/users/twhitacre' ).done( function (data) {
  console.log(data);
});
```

## Promises

```js
$.getJSON( 'https://api.github.com/users/twhitacre' )
 .done(function(){
   console.log("first")
 })
 .always(function(){
   console.log("second")
 })
 .done(function(){
   console.log("third")
});
```


## POST

```js
$.ajax( URL, {
   type: "POST",
   dataType: 'json',
   data: {
     name: 'tim',
		 age: 30,
		 location: 'Atlanta'
   }
})
```
