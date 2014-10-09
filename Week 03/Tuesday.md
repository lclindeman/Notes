## jQuery

Injecting / Interacting with data

```html
<div class="container">
  <h3 class="title">Hello World</h3>
  <article class="content">I am some comtent</article>
</div>
```

```js
$('.title').text() // grabs the text inside of the element
$('.container').html() // grabs the HTML inside of the element

// Replace
$('.title').text('New Title') // sets the text inside of the element
$('.container').html('<a href="http://google.com">Google</a>') // sets the HTML inside of the element

// Append
$('.container').append('<a href="http://google.com">Google</a>');

// Prepend
$('.container').prepend('<a href="http://google.com">Google</a>');

```


## HTTP

* Hypertext Transfer Protocol
* HTTP is the protocol that allows for sending documents back and forth on the web.


## RESTful API's

* REST : Representational state transfer
* REST is an architecture style.


### Methods CRUD
- GET: fetches the resource - Read
- POST: create the resource - Create
- PUT: update the resource - Update
- DELETE: deletes the resource. - Delete


#### Create - POST

`/artists/new`

=> Allows you to send in a set of data to create a new artist

#### Read - GET

`/artists`

=> Returns an array of all artists

`/artists/beartooth`

=> Returns an array of information about the artist Beartooth

#### Update - PUT

`/artists/edit/beartooth`

=> Sends in data to edit a the data on the artist Beartooth

#### Delete - DELETE

`/artists/delete/beartooth`

=> Removes the artist Beartooth from our database

## Statuses
http://httpstatus.es/
The ones you should be most familiar with:
- 200
- 201
- 400
- 404
- 401
- 500

## SoundCloud API Fun

[SoundCloud Payload](http://cl.ly/code/123j120m163I)

```js
var container = $('#tracks'),
    song_image, song_title, song_mp3, track;

rocktracks.forEach( function (song) {

  // Build Image Tag for Each Song
  song_image = "<img src='" + song.artwork_url + "' />'";

  // Build Image Title
  song_title = "<p>" + song.title + "</p>";

  // Build the Song MP3
  song_mp3 = "<audio controls src='" + song.stream_url + "?client_id=87322f9fd4d27754fc7adf00ce869254'></audio>";

  // Build Each Track Display
  track = "<li>" + song_title + song_mp3  + song_image + "<hr /></li>";

  // Append Each Track To my Tracks List
  container.append(track);

});
```
