# Git

and how to use it

---

# Part One

Overview of terminology, basic use and commands

---

## RCS, VCS, SVC, SVM, SCM

* Version Control System
* Software Version Control
* Revision Control System
* Software Version Management
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

* Name is a play on the slang term
* Git was self hosted a day after release
* Merges into Git with Git happened a week later
* Achieved all performance goals

This is straight from Wikipedia:
https://en.wikipedia.org/wiki/Git#History

---

## Uses

### _Software Verson Control_

#### Control, backup, archive non-binary files

* Track Changes
* Upload to mulitple sources
* Pull down
* Find removed files at any point
* Maintain two versions of the same file
* Create tag checkpoints for the entire repo

Note:

* Any file with some config (git-lfs)
* https://git-lfs.github.com/

---

# Command Overview

---

## `git init`

> Initialize a git repository inside a folder

* Sets you up to track files and folders within this folder

---

## `git status`

> See the status of your repository

* If you have uncommitted changes
* If you have pending remote changes
* What branch you are on

---

## `git add`

> Add files to your next commit

* _Stages_ these files
* Your next commit will include these files
* You _have_ to add files to commit

---

## `git reset`

> Remove all files from your next commit

* _Unstages_ these files
* Your next commit will not include these files
* __Does not__ remove your changes

---

## `git commit`

> Commit your changes to the history

* Now its for real
* Records the commit into the history
* Your changes are not 'staged' anymore
* You can now push to a remote

---

## `git checkout`

> Checkout version, commit, tag, in your history

* Go back in the history
* Go forward in the history
* Checkout specific files, to undo changes

---

## `git tag`

> Add a 'checkpoint' to reference

* reference a point in your history
* commonly used for versions
* can attach information to a tag

Note:

* You should attach release notes to your tags

---

## `git log`

> Print the history

* Shows you the history of your repository, along with the hashes
* Formatting available
* Shows authors as well

Note:

* Should be formatted

---

## `git diff`

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
* Commit messages can be for both humans and computers
  _but more for humans_

Note:

* Would you put a candy wrapper in your filing cabinet
* To be a little frank

---

## Commit Standards

> https://conventionalcommits.org/

* Started by angular (google)
* Used by lots of people now
* Also, tools use it to create changelogs automatically

---

# Part Two

Exploring Rebasing, History and Merge Conflicts

---

## What is Rebasing

<!-- ![git rebase origin master](git/git-rebase-origin-master.png) -->

* Useful tool for managing branches of code
* Moving changes around within the history
* Removing, renaming, combining commits

Note:

* Any project with branches will need to move commits
* Moving to a new 'parent' commit

---

## The Rebase Command

<!-- ![git rebase help](git/git-rebase-help.png) -->

* tonnes of options
* can be as simple or as complicated as needed
* best used on local branches __before pushed to the remote__

> "With great power comes great responsibility - uncle ben" - michael scott

Note:

* Merging, interactive, onto, keep merges
* you can fuck shit up with ease

---

## Flag Overview

---

### `-i --interactive`

`git rebase -i`

* Introduces an interactive 'middle' step
* Allows for reordering, renaming, removing, merging commits
* Useful for updating a branch before submitting it for review

---

### `--onto`

* Changes the base of the branch you are targeting

`git rebase --onto master next topic`

* master is the target
* next is previous root
* topic is the branch you are using

---

### `-p --preserve-merges`

`git rebase master --preserve-merges`

* tries to preserve the merge commits and actions from previous merges
* for keeping history, if rebasing and then merging into same branch (otherwise you lose the merge commits)

---

## Merge Strategies

---

### Recursive (default)

* uses three-way merge ([inspects changes](https://stackoverflow.com/a/4129145))
* ours / theirs strategies

---

### Octopus

* useful for merging feature branches
* add feature branches into a release branch

---

### Ours

* keeps history but throw away __all__ changes made in other branch
* commits will be there, but nothing else

---

## Rebasing with master

---

## Rebasing onto a branch

---

## Rebasing with HEAD

---

## Dealing With Conflicts

---

### General Format

* two versions have changed the same lines, we cant merge them together without making a decision
* adds lines to the files, displays both conflicting versions

```text
If you have isues please
<<<<<<< BASE_BRANCH (Current Change)
open an issue.
=======
ask your question in slack.
>>>>>>> OTHER_BRANCH (Incoming Change)
```

* `BASE_BRANCH` is _your_ version - might display `HEAD`
* `OTHER_BRANCH` is _their_ version

---

### "Current" and "Incoming" (Yours, Theirs)

* If you are merging into _your_ branch, your change is `current`
* If you are merging into _their branch_ (or master), your change is `incoming`

Note:

The branch that you are merging into is always the current. To merge in a branch you were working on,
you would have to move to the base branch first.

---

## Questions
