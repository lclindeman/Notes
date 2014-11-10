## BackboneJS Router

> Provides methods for routing client-side pages, and connecting them to actions and events. For browsers which don't yet support the History API, the Router handles graceful fallback and transparent translation to the fragment version of the URL.


> Client Side vs Server Side 


## So BackboneJS Routers?

* Allows you to navigate through the app with out page load
* Allows you to create bookmarkable links in a SPA


## When do we need one?

* Large view change
* Need for bookmarkable link


```js
 var PostRouter = Backbone.Router.extend({
     initialize: function () {
           Backbone.history.start();
             },
               routes: {
                     "posts/:id": "getPost"
                       },
                         getPost: function (id) {
                               alert("Loading Post " + id);
                                 }
 });

 // Create an Instance
 var post_router = new PostRouter();
 ```

