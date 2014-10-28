
## Review on File Structure && Pop Quiz

We started out today with a "pop" quiz. Basically an excercise to see any weekness that we have developed in our dependencies on Yeoman.

You can view the quiz [here](https://gist.github.com/twhitacre/833ef11d45f5fd2785cb).


## Testing 101

Unit Testing

> Unit testing is the practice of testing specific areas or "units" of our code.

Pros:

* Helps to identify failures in your code. Especially helpful as our codebase grows.
* Forces you to write better code
* Prevents code from breaking in the future

Cons:

* Time commitment

## Testing Frameworks

* [QUnit](http://qunitjs.com/)
* [Jasmine](http://jasmine.github.io/)
* [Mocha](http://mochajs.org/)


## Mocha

> Mocha is a feature-rich JavaScript test framework running on node.js and the browser, making asynchronous testing simple and fun.


## Chai

> Chai is a BDD / TDD assertion library for node and the browser that can be delightfully paired with any javascript testing framework.


## TDD vs BDD

#### TDD = Test Driven Development

> The idea of writing tests first, having them all fail (because of no code) then writing tests to make the code pass.

#### BDD = Behavior Driven Development

> At it's core, BDD is a feature driven approach to TDD. Very similar to TDD but more verbose. The same approach is taken but here we write our tests to read like sentences. BDD is more focused on the features as opposed to the results.

## Demos

```js
var Cat = function (options) {
  options = options || {};
  this.color = options.color || 'brown';
  this.status = 'grumpy';
  this.pet = function () {
    this.status = 'happy';
  };
};
```

```js
var cat;

describe('My Cat Object', function () {

  // Test creation of instance
  describe('Creating a new cat', function () {

    beforeEach(function(){
      cat = new Cat();
    });

    it('should be an instance of Cat', function () {
      expect(cat).to.be.an.instanceof(Cat);
    });

    it('should have a default color', function () {
      expect(cat.color).to.equal('brown');
    });

    it('should have a status that is a string', function () {
      expect(cat).to.have.property('status');
    });

    it('should be grumpy by default', function () {
      expect(cat.status).to.equal('grumpy');
    });

    it('should be happy after I pet it', function () {
      expect(cat.status).to.equal('grumpy');
      cat.pet();
      expect(cat.status).to.equal('happy');
    });

  });


});
```