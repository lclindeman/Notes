## Deploy a Yeoman Web App on Heroku

#### Prerequisites - [Heroku Toolbelt](https://toolbelt.heroku.com/)

1: Navigate to any Yeoman App

2: You'll need Express and Gzippo so run the following

 * `npm install gzippo --save`
 * `npm install express --save`


3: Create a `web.js` in root (`touch web.js`) and add the following:

```js
var gzippo = require('gzippo');
var express = require('express');
var app = express();

app.use(gzippo.staticGzip("" + __dirname + "/dist"));
app.listen(process.env.PORT || 5000);
```

4: Create a Procfile in root (`touch Procfile`) and add the following:

```js
web: node web.js
```

5: Create our Heroku app with `heroku create`

> You can still run git as normal. `git add .` then `git commit -m "Commit Message"`

6: Then `git push heroku master`

> Voila! Your project should be on Heroku now!

7: Don't forget to still push to Github, `git push origin master`

-------

### Did something break?

At this point your best bet is to debug with `foreman`. Try running `foreman start` and see what happens. If this fails, then you have problems which is likely why your app will not load up on Heroku. Fix this and you should be good.
