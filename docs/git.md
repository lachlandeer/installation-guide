## Git

Git is my go to version control system.

It's usually installed on Ubuntu when you install the OS. 
The last time I did this though, it was not.
Install it:

```
sudo apt-get install git
```

## Basic Set Up

To use Git we need to have some basic configuration set up.
If we forget to do this, the first time we try and commit something we will be prompted for it.

```
$ git config --global user.name "FirstName LastName"
$ git config --global user.email "something@domain.somethingelse"
```

In addition, instead of Git opening Vim when it wants further information, I prefer it to open nano:

```
$ git config --global core.editor "nano -w"
```

And to handle line endings in a way that Windows can also deal with (this is totally optional):

```
$ git config --global core.autocrlf input
```

## Introductions to Git / Where to look for help:

* Software Carpentry's [Version Control with Git](http://swcarpentry.github.io/git-novice/)
* PP4RS' [Introduction to Git](https://github.com/pp4rs/2019-foundations-uzh-material/raw/master/03-git-local/git-local.pdf)
