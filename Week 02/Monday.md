## Computer Setup

This will make sure you have the following installed:

* Mavericks
* XCode
* Homebrew
* git
* Atom

Also Checks that:

* Atom is the default git editor
* Github SSH

```sh
$ curl -s https://gist.githubusercontent.com/twhitacre/24dd3b04f3265cd31fc1/raw/a6eaa774b4fc3682f7dcacc6ab1ec9fa203eeb55/check.sh | bash
```
___Thanks [Jake](https://github.com/jacobthemyth)!___

## Homework Review

* [S&P Share Buttons](http://codepen.io/twhitacre/pen/oHnsE?editors=110)
* [S&P Blue Boxes](http://codepen.io/twhitacre/pen/Hlxjc?editors=110)


## Git Branching

```sh
$ git branch my-new-branch
$ git checkout my-new branch
```

Short cut method. Creates and checks out a branch in one command

```sh
$ git checkout -b my-new-branch
```

## Git Merging

```sh
$ git checkout master
$ git merge my-new-branch
```

## Sass

#### Installing Sass

Documentation - http://sass-lang.com/

```sh
$ gem install sass
$ sass -v
```

## Sass Demo

#### Processing Sass

```sh
# Compile once
$ sass input.scss output.css

# Or Watch your files
$ sass --watch input.scss output.css
```

#### Variables
```css
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```

#### Nesting

```css
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

#### Partials & Imports

`_reset.scss` - Normalize?

```css
@import 'reset';

body {
  font-size: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```

#### Mixins

```css
@mixin border-radius($radius) {
  border-radius: $radius;
}

.box { @include border-radius(10px); }
```

#### Operators

```css
.container { width: 100%; }

article[role="main"] {
  float: left;
  width: 600px / 960px * 100%;
}

aside[role="complimentary"] {
  float: right;
  width: 300px / 960px * 100%;
}
```

## Github Pages

Documentation - https://pages.github.com/

Create a branch called `gh-pages`

http://username.github.io/project-name
