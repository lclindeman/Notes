## JavaScript `this`

A function's `this` keyword behaves a little differently in JavaScript compared to other languages. It also has some differences between strict mode and non-strict mode.

We use `this` similar to how we use pronouns in the English language.

> Tim is a teacher at The Iron Yard, he really enjoys it.

In the above sentence, _he_ is referring to _Tim_

In JavaScript, `this` can refer to many different things depending on the context in which it is used.  

## Constructors

The constructor property is a reference to the function that created an object.

## JavaScript `new` Keyword

The `new` operator creates an instance of a user-defined object type or of one of the built-in object types that has a constructor function.


## Prototype

> Not to be confused with [Prototype](http://prototypejs.org/) the JS Library

Prototypes allow you to easily define methods to all instances of a particular object. The beauty is that the method is applied to the prototype, so it is only stored in the memory once, but every instance of the object has access to it

Has to do with inheritance.

> Every object in JavaScript has a prototype.

Prototype inheritance chains can go as long as you want. But in general it is not a good idea to make long chains as your code can get difficult to understand and maintain.


## Demos


#### Inheritance Chain

> The call() method calls a function with a given `this` value and arguments provided individually.

```js
function Pet(name, species){
    this.name = name;
    this.species = species;
}
function view(){
    return this.name + " is a " + this.species + "!";
}
Pet.prototype.view = view;

function Dog(name){
    Pet.call(this, name, "dog");
}

Dog.prototype = new Pet();
Dog.prototype.bark = function(){
    console.log("Woof!");
}
```

#### Basic Demos

```js
// Person Constructor
var Person = function (options) {
  var options = options || {};
  this.name = options.name;
  this.age = options.age;
  this.sex = options.sex;
  this.location = options.location;
  this.drive = function (driven, new_condition) {
    driven.condition = new_condition;
  }
};
```

```js
// Create a Prototype
Person.prototype.greeting = function () {
    var str = this.name + ' is ' + this.age + ' years old and currently lives in ' + this.location;
        str += '<br /><br />';
    console.log(str);
};
```

```js
// New Person
var personA = new Person ({
  name: 'Bob',
  age: 30,
  sex: 'male',
  location: 'Atlanta'
});
// personA.greeting();
```

```js
// Car Constructor
var Car = function (options) {
  var options = options || {};
  this.make = options.make;
  this.color = options.color;
  this.condition = options.condition || 'New';
};
```

```js
// New Car
var accord = new Car({
  make: 'Honda',
  color: 'Red',
  condition: 'Used'
});
```

```js
// Playing with Both
accord.owner = personB;
personA.drive(accord, 'Wrecked');
console.log(accord.owner.name);
```

## Resources 

* [Consctuctors](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/constructor)
* [Understanding Prototypes](http://yehudakatz.com/2011/08/12/understanding-prototypes-in-javascript/)
* 