# AngularJS

Let's talk about what it is, where it came from and some of the "parts" of it. Remember this is just an introduction to it.


## What is AngularJS?

> A client-side Framework for adding interactivity to our HTML.<br /><br />

> You can think of it as HTML enhanced for web apps.


## History & Future

> Originally created in 2010 by Misko Hevery and Adam Abrons, now run by the Google team. <br /><br />

> Google’s Vision for what a browser would be like if if was built from the ground up. <br /><br />

> Google’s vision for web components - see Angular v2.0


## Two Parts to Angular

1. UI - Declarative - What you would like to happen.
2. App - Imperative - Telling the machine what to do.


## Why use AngularJS?

* Helps with organization of JavaScript
* Works well with other libraries like jQuery
* Ability to create extremely fast websites
* It is easy to write tests for


## Model

> The model is made up of plain JS objects. No need for inheriting or extending. We also don't need to use any special getter/setter methods to access it. This means that we write less boilerplate code.


## ViewModel

> It is an object that provides specific data and methods to maintain a specific view. `$scope` is just a regular JS object with a small API created to detect broadcast changes to its state.


## Controller

> The controller is used for setting initial state and mutating the `$scope` with methods.


## View

The view is the HTML that exists after AngularJS has parsed and compiled the HTML to included rendered markup and bindings.


## `$scope`

> The `$scope` has a reference to the data, the controller defines the behavior and the view handles the layout and hands off interaction to the controller to respond accordingly. 


## Module

> A method that instantiates and wires together the different parts of the application.

```js
var app = angular.module('whatever', []);
```


## TWO-WAY DATA BINDING

> AKA, The Magic of AngularJS


## Directives

> A directive is a marker on a HTML tag that tells AngularJS to run or reference some JS code.

Some common ones:

* `ng-repeat`
* `ng-click`
* `ng-show`
* `ng-class`


## Demos

```js

var app = angular.module('PeopleList', []);


app.controller('PersonController', function ($scope) {

  $scope.people = [
    {
      name: 'Tim',
      age: 31,
      test: true
    },
    {
      name: 'Bob',
      age: 45,
      test: false
    },
    {
      name: 'Sam',
      age: 113,
      test: true
    }
  ];

  $scope.hello = function (n, i) {
    if($scope.people[i].name === 'Tim') {
      alert('go away');
    } else {
      alert('Hi there ' + n + ' and I am number ' + i);
    }
  };

});
```

```html
<body ng-app="PeopleList">

    <div class="hero-unit">
      <h1>Angular</h1>
      <div class="something" ng-controller="PersonController">
        <p ng-repeat="p in people">
          {{ $index + 1 }} - Hi, my name is {{ p.name }} and I am {{ p.age - 5 }} years old. 
          <a ng-show="p.test" href="" ng-click="hello(p.name, $index)">Say Hi</a>
        </p>
      </div>
    </div>

    <!-- build:js scripts/vendor.js -->
    <!-- bower:js -->
    <script src="../bower_components/jquery/dist/jquery.js"></script>
    <script src="../bower_components/underscore/underscore.js"></script>
    <script src="../bower_components/angular/angular.min.js"></script>
    <script src="../bower_components/angular-route/angular-route.min.js"></script>
    <!-- endbower -->
    <!-- endbuild -->

    <!-- build:js scripts/main.js -->
    <script src="scripts/main.js"></script>
    <!-- endbuild -->

  </body>
```
