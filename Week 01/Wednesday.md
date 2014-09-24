# Wednesday

Today we installed...

* Atom
* iTerm 2
* Oh My ZSH
* XCODE Command Line Tools

More info on those can be found [here](http://tiy-atlanta-js.github.io/tools.html).

## Intro to Terminal

```sh
# make a directory
$ mkdir <directory-name>

# move into a directory
$ cd <directory-name>

# list the contents of a directory
$ ls

# the symbol for the parent directory is ..
$ cd .. # this moves up one directory

# See the current directory
$ pwd
```

## Git Commands

#### Creating a repository on your computer
This creates a git repository in the current directory.

```sh
git init
```

#### Adding files to the staging area

To see the current status of your directory and repository:

```sh
$ git status
```

To track *all* files. You can do this by adding the current directory.

```sh
$ git add .
```

#### Checking the status
```sh
$ git status
```

#### Committing files
Now that you have files in the staging area, you can save a snapshot of the staging area using a commit.

```sh
$ git commit -m "Message"
```

#### Edit Default Git Editor (change to Atom)

```sh
git config --global core.editor "atom --wait"
```

## Resources

* [Octocat Code From Homework](https://gist.github.com/twhitacre/8da056b0be14ae25a828)
* [Practice git](https://try.github.io/levels/1/challenges/1)
* [Official git Docs](http://git-scm.com/)
