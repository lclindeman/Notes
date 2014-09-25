## Github Intro

  * Set up auth keys
  * Everything needs a `Readme.md` file
  * `git push` vs `git pull`

> Remember, every repo should have a readme.md file.

![alt text](http://f.cl.ly/items/1t3V1U0E0I2e0l0H0028/opsmall.gif "You get a readme!!!")

## Creating a NEW Project

1. Create a new repo on Github.com
2. Clone that down to your project directory on your computer

	```sh
	# Make sure to copy the correct SSH url
	$ git clone git@github.com:tiy-atlanta-js/Notes.git
	```

3. Navigate into that folder

## Working with an EXISTING Project

1. Create a new repo on Github.com
2. Navigate into your project folder
3. Add the remote origin from the gh project to your local project

	```sh
	# Again, make sure to copy the correct SSH url
	$ git add remote origin git@github.com:tiy-atlanta-js/Notes.git
	```

## Changes on Github.com

To check for changes on Github.com you can pull down the repo

```sh
# You can fetch
$ git fetch

# And you can pull, just like you push
$ git pull origin master
```

## HTML Elements

* header
* footer
* nav
* section
* article
* main

## CSS Notes

  * [The Ah-Ha Moment](http://css-tricks.com/the-css-ah-ha-moment/)
  * Every page element is a box.
  * I can control the size and position of those boxes.
  * I can give those boxes background images.


## CSS Element Width Formula

  > Width = width + padding-left + padding-right + border-left + border-right


  > Height = height + padding-top + padding-bottom + border-top + border-bottom

## CSS Hovers

  * pseudo class `:hover`
  * CSS3 Prefixes
  * [CSS3/HTML5 Support](http://caniuse.com/)
  * Multiple Selectors


## Resources

* [Surf & Paddle Mockup](http://codepen.io/twhitacre/full/8360ef72df7751b9487b24993d9b2e30/)
* [Setting Up SSH Keys](https://help.github.com/articles/generating-ssh-keys)
* [Github Markdown](https://help.github.com/articles/github-flavored-markdown)
* [CSS Specificity](http://css-tricks.com/specifics-on-css-specificity/)
