# Git

and how to use it

---

## RCS, VCS, SVC, SVM, SCM?!

* Version Control System
* Software Version Control
* Revision Control System
* Software Versom Management
* Software Configuration Management
* Software Change Management?
* Source Code Management?!

These are all about the same thing.

Note:

* Git has dubbed itself an _SCM_.
* These mean the same thing, but have different interpretations
* Different Software or companies tend to use different acronyms

Here is a SO that explains it more: https://stackoverflow.com/questions/5872136/difference-between-scm-and-svn

---

## A brief history of Git

* Started for Linux in 2005
* Quick adoption
* Junio Hamano took over four months later and remains the core maintainer

Note:

* Git was self hosted a day after release
* Merges into Git with Git happened a week later
* Achieved all performance goals

This is straight from Wikipedia:
https://en.wikipedia.org/wiki/Git#History

---

## Uses

#### _Software Verson Control_

**Control, backup, archive non-binary files**

* Track Changes
* Upload to mulitple sources
* Pull down
* Find removed files at any point
* Maintain two versions of the same file
* Create tag checkpoints for the entire repo

Note:

* Any file with some config (git-lfs)

---

## Follow Along Tutorial

#### try.github.io

And the cheatsheet reference you might want to save
https://gist.github.com/hofmannsven/6814451

---

# Command Overview

---

### `git init`

> Initialize a git repository inside a folder

* Sets you up to track files and folders within this folder

---

### `git status`

> See the status of your repository

* If you have uncommitted changes
* If you have pending remote changes
* What branch you are on

---

### `git add`

> Add files to your next commit

* _Stages_ these files
* Your next commit will include these files
* You _have_ to add files to commit

---

### `git reset`

> Remove all files from your next commit

* _Unstages_ these files
* Your next commit will not include these files
* __Does not__ remove your changes

---

### `git commit`

> Commit your changes to the history

* Now its for real
* The commit is added to the history
* Your changes are not staged anymore
* You can now push to a remote

---

### `git checkout`

> Checkout version, commit, tag, in your history

* Go back in the history
* Go forward in the history
* Checkout specific files, to undo changes

---

### `git tag`

> Add a 'checkpoint' to reference

* reference a point in your history
* very commonly used for versions
* can attach information to a tag

Note:

* You should attach release notes to your tags

---

### `git log`

> Print the history

* Shows you the history of your repository, along with the hashes
* Can be formatted
* Shows authors as well

Note:

* Should be formatted

---

### `git diff`

> Show the changes or differences between commits

* Shows the current unstaged additions and deletions
* Shows the differences between two commits

---

# Authentication & Remote Repositories

_The cloud_

Other people's computers  
<sub><small>_or your other computer_</small></sub>

---

## Methods

* HTTPS
* SSH

SSH is a highly preferred method of authentication  
You can use HTTPS if you like typing in passwords

---

## Setting up SSH (server specific)

* Lets walk through how to setup SSH within github
* Give your public key to the server
* Prove you are you with the private key

---

## Commands

* **`git remote`**: list, add, remove remote sources
* **`git fetch`**: fetch from a remote
* **`git pull`**: pull from a remote
* **`git push`**: push to a remote

---

# Authoring Practices

> How to make good commits and why they matter

---

## Purpose and Importance of making good commits

* Why keep a history if you are going to fill it up with trash
* You aren't going to remember what you wanted to say
* So say what you wanted to say
* Don't get lazy, commitments are forever
* Commits are for both humans and computers
  _but more for humans_

Note:

* Would you put a candy wrapper in your filing cabinet
* To be a little frank

---

### Some real life commits

* [This one is by me](https://github.com/forstermatth/sa-puppies/commits/master)
* [This one is in a joke repo](https://github.com/Donohue/Shamebot/commits/master)
* [This might be malicous code](https://github.com/caseyscarborough/keylogger/commits/master)

---

## Commit Standards

> https://conventionalcommits.org/

* Started by angular
* Used by lots of people now
* Also, tools use it to create changelogs automatically

---

# Resources

You can see these slides at this URL or at https://github.com/codeyql/talks

* Cheatsheet: https://gist.github.com/hofmannsven/6814451
* Presentation Platform: https://gitpitch.com

---

### Part Two, How not to rebase
