## Intro to Parse.com

> Parse is a BaaS (Backend as a Service) that can replace the need for a simple backend and allow us to create fully functional applications.

## Basic Usage

1. Sign up for a Parse.com Account
2. Create a new app
3. Under "select a produce" choose
  * Data
  * Web
  * Exsisting Project
4. Copy the path to their CDN
  * Similiar to `<script src="//www.parsecdn.com/js/parse-1.3.1.min.js"></script>`
5. Add that to your project where you would normally call Backbone
  > Note! You need to make sure to add this OUTSIDE of any Gulp/Bower build tags
6. Copy your App id and Secret
  * Similiar to `Parse.initialize("xxxxxx", "xxxxxx");`
7. Paste this before you initiate any Parse calls


## Converting Backbone to Parse

> There's a [guide](https://www.parse.com/docs/js_guide#convert) for that!

Basically though, 

* `Backbone.Model` => `Parse.Object`
* `Backbone.Collection` => `Parse.Collection`
* `Backbone.View` => `Parse.View`
* `Backbone.Router` => `Parse.Router`
* `Backbone.history` => `Parse.history`
* ... and so on


## Resources

!! [All The Docs!](https://www.parse.com/docs/js_guide#javascript_guide) !!!
