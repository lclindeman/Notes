## Review of Creating our own library

> [Go Here for an Example](https://gist.github.com/twhitacre/22bde2a881d54137f3dd)

## Deployment

A general process for pushing your application to a remote server and making it live for others to view.

## PaaS vs Hosting

* Heroku
* Firebase
* Nodejitsu
* Digital Ocean

## Heroku

Cloud computing designed and built for developers.

Ruby, Node.js, Python, PHP and Java

Deploy with Git and Heroku tracks Releases

* Sign Up at Heroku.com
* Install the Heroku Toolbelt
* Login to Heroku (SSH Key) - [Info Here](https://devcenter.heroku.com/articles/keys)
  * Simply run `heroku login` from command line
* Deploy Your App -- See Below

> Procfile is a mechanism for declaring what commands are run by your application's dynos on the Heroku platform. It follows the process model. You can use a Procfile to declare various process types, such as multiple types of workers, a singleton process like a clock, or a consumer of the Twitter streaming API.

## Node & Express

Node: A platform built on Chrome's JavaScript runtime for easily building fast, scalable network applications.

Express : Web application framework for Node and provides a thin layer of features fundamental to any web application.

Here is a simple Node App:

```js
var http = require('http');

http.createServer(function (req, res) {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello World\n');
}).listen(3000, '127.0.0.1');

console.log('Server running at http://localhost:3000/');
```
Then run it: `$ node server.js`

## Deploy Yeoman App on Heroku with Express

1. Create Yo App
2. Install Express & Gzippo (explain this)
3. Create a `web.js` or `server.js` file
4. Create a `Procfile` file
5. Run `$ heroku create`
6. Git as usual
7. Deploy `$ git push heroku master`


> [Deployment Directions](https://github.com/tiy-atlanta-js/Notes/blob/master/Heroku_Deployment.md)
