## Single Page Applications

* Gmail
* Google Docs
* [Unmark](http://unmark.it)


## JavaScript Frameworks & Libraries

Let's first look at what a standard MVC looks like


## MODELS

They represent the data in your application. This can be viewed as a type of data you can model, like a Person, User, Car, ToDo etc. Models should always be up to date and be able to notify anyone about their current state.


## Views

They are what the user of your application interfaces with. Views are always aware of your Models but don't directly communicate with them.


## Controllers

They handle the actions. They take input, watch for clicks and other user actions. Basically Controllers handle the input while Views handle the output. A controller will update your Modal and then because of the relationship with the view it will be updated there. Note though that your controller does not talk to your view.


# Backbone.JS

Backbone.js gives structure to web applications by providing models with key-value binding and custom events, collections with a rich API of enumerable functions, views with declarative event handling, and connects it all to your existing API over a RESTful JSON interface.

Some frameworks... like Backbone... don't really have Controllers, but pass off the responsibility of what a Controller normally does to the View. 


## Backbone.JS Parts

* Models
* Views
* Collections
* Routes


The cool thing about Backbone as opposed to other MVC(ish) Frameworks is that all of these parts are independent. They don't require each other to work and you are free to choose when and if you pick any of them.


## Backbone.JS Models

Basically a Backbone Model is a constructor that determines the shape that your data will be.<br><br>

Backbone.Model is basically just a plain old constructor. It does have one fancy method though. In fact all of the parts of Backbone do. It's the `extend` method.


## Backbone.JS Extend Method

In Backbone's world, `extend` means "take this object literal, use it's properties and methods and overwrite any conflicting properties". Its cool because you end up with your own customized version of Backbone.Model.


```js
var TimsCoolModel = Backbone.Model.extend ({

  initialize: function () {
    console.log("I'm doing programming!!");
  }

});
```

## NOOP

An empty function<br><br>

A noop is a function that doesn't do anything and has no return value (other than default `undefined`).<br><br>

Why have these? Well they are there for us to fill in as we need to.<br><br>


## BackboneJS Model Instance

```js
var coolInstance = new TimsCoolModel({
  name: "Fido",
  type: "Dog",
  cool: true
});
```

## How Do We Access Properties?

get: `model.get();`

set: `model.set();`


## BackboneJS Collections

They are a pretty simple mechanism. Collections are meant to store an array of model instances and also house methods that are useful for working with a group of models.

```js
var TimsCoolCollection = Backbone.Collection.extend ({

  model: TimsCoolModel,
  url: 'http://my-api-url-endpoint'

});
```


## Demos

#### Model

```js
var Student = Backbone.Model.extend ({

  defaults: {
    name: '',
    location: 'Atlanta',
    awesome: true
  },

  idAttribute: "_id",

  initialize: function () {
    var name = this.get('name');
    console.log( name + ' has been added to your list of students.');
  }

});
```

#### Collection

```js
var JSStudents = Backbone.Collection.extend ({

  model: Student,
  url: "http://tiy-atl-fe-server.herokuapp.com/collections/students"

});
```

#### Using them

```js

// Instance of our Collection
var all_students = new JSStudents();


// Getting our data
all_students.fetch().done(function () {
  console.log(all_students);
});


// Adding More Data
var bob = new Student({ name: 'Bob' });
all_students.add(bob).save();
```