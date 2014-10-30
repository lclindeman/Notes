## Code Challenges

Check them out [Here](http://www.sitepoint.com/5-typical-javascript-interview-exercises/)


## FizzBuzz

#### Question

> Write a program that prints the numbers from 1 to 100. But for multiples of three print “Fizz” instead of the number and for the multiples of five print “Buzz”. For numbers which are multiples of both three and five print “FizzBuzz”.

#### Answers

```js
for (var i=1; i <= 100; i++) {
  if (i % 15 == 0) {
    console.log("FizzBuzz");
  } else if (i % 3 == 0) {
    console.log("Fizz");
  } else if (i % 5 == 0) {
    console.log("Buzz");
  } else {
    console.log(i);
  }
}
```

```js
for(i=0;i<100;)console.log((++i%3?'':'Fizz')+(i%5?'':'Buzz')||i)
```

## Persistent Data

That can be seen [here](https://github.com/tiy-atlanta-js/Simple_ToDo)