## Backbone View Review

> Continue to use [this app](https://github.com/tiy-atlanta-js/Backbone_Feels) to follow along for yesterday and today.

#### Events

```js
events: {
  "click .done": "markAsDone"
},

markAsDone: function(){
  this.model.set('done', true).save();
},
```

## Module Pattern

```js
// type window to communicate intent
window.App = {};

// This is for view constructors, not instances.
App.Views = {};
App.Models = {};
App.Collections = {};
App.Routers = {};
```