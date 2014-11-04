## Backbone Review

* What is a Model?
* What is a Collection?
* How can they relate?


## Backbone Model & Collection Review

To really grasp models vs collections... think of it this way.

`Backbone.Collection` is a collection of `Backbone.Model`'s. Take the examples below... as Model => Collection:

* `Animal` => `Zoo`
* `Todo Item` => `Todo List`
* `Brother/Sister` => `Family`

Typically your collection will only use one type of model but models themselves are not limited to a type of collection...

* `Todo Item` => `Todo List`
* `Todo Item` => `Grocery List`
* `Todo Item` => `Shopping List`

## Backbone View

> Backbone Views are the mechanism you'll almost always use for getting your data into the page. They don't "do" much by default, which throws off most people. Like most of the rest of Backbone, you have to be rather explicit about what you want to happen. Once you adjust to the fact that there is very little magic, though, they can be pretty handy. Think of Backbone Views as a Trapper Keeper® for what would otherwise be a garbled mess of jQuery events.

```js
var PersonView = Backbone.View.extend({

  el: $('.hero-unit'),

  initialize: function () {
    this.render();
  },

  render: function () {
    this.$el.html('Hai Guyz!');
  }

});
```

Let's talk about the following:

* `initialize`
* `render`
* `el`
* `$el`

The rationale here is that we only want to put this.el into the page once, but we may want to render and re-render multiple times. If you think of this.el as a sort of shell or container, which we will fill with content later, the purpose is easier to grast. Thus we've decoupled injection into the page from content rendering.