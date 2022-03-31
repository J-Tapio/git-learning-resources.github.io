# Git related learning resources

Cheat Sheets & Learning resources combined from different sources.

> Own notes highlighted this way.

___

## Git

**_Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
Git is easy to learn and has a tiny footprint with lightning fast performance. It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenient staging areas, and multiple workflows._** [-Git](https://git-scm.com)

## GitHub

**_GitHub is a web-based Git repository hosting service, which offers all of the distributed revision control and source code management (SCM) functionality of Git as well as adding its own features._** [-GeeksForGeeks](https://www.geeksforgeeks.org/difference-between-git-and-github/)
___

## Learning Resources

### Cheat sheets

#### Atlassian Git Cheat Sheet

* [Atlassian Git Cheat Sheet](chrome-extension://ihgdgpjankaehldoaimdlekdidkjfghe/viewer.html#https://wac-cdn.atlassian.com/dam/jcr:e7e22f25-bba2-4ef1-a197-53f46b6df4a5/SWTM-2088_Atlassian-Git-Cheatsheet.pdf?cdnVersion=289)

#### GitHub cheat sheet

* [GitHub Cheat Sheet](chrome-extension://ihgdgpjankaehldoaimdlekdidkjfghe/viewer.html#https://education.github.com/git-cheat-sheet-education.pdf)

#### Git cheat sheet

* [Git Cheat Sheet PDF - topic related cheat sheets](https://training.github.com)
* [Interactive/Visual Cheat Sheet](https://ndpsoftware.com/git-cheatsheet.html)

### Free Learning Resources

#### Atlassian Git Tutorial

* [Become a git guru.](https://www.atlassian.com/git/tutorials)

#### Microsoft Learning

* [Introduction to GitHub](https://docs.microsoft.com/en-us/learn/modules/introduction-to-github/)

#### Udemy

* [Learn Git: Everything You Need To Know](https://www.udemy.com/course/learngit/)

#### freeCodeCamp

* [Learn the Basics of Git in under 10 minutes](https://www.freecodecamp.org/news/learn-the-basics-of-git-in-under-10-minutes-da548267cc91/)
* [Git and GitHub Tutorial - Version Control for Beginners](https://www.freecodecamp.org/news/git-and-github-for-beginners/)

#### w3Schools

* [Git Tutorial](https://www.w3schools.com/git/default.asp)

#### Learn Git Branching - Interactive tutorial

* [Learn Git Branching](https://learngitbranching.js.org)

#### GitHub Learning Lab

* [Github Learning Lab](https://lab.github.com)

#### Git Tower

* [Learn Version Control with Git](https://www.git-tower.com/learn/git/ebook/)

#### Udacity

* [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)

#### GitKraken

* [Learn Git - Commands, Tutorials & More](https://www.gitkraken.com/learn/git)

#### Eduonix

* [GIT for beginners](https://www.eduonix.com/git-for-beginners)

#### Git Immersion

* [A guided tour that walks through the fundamentals of Git, inspired by the premise that to know a thing is to do it](https://gitimmersion.com)

#### Visual Git Reference - Mark Lodato

* [A Visual Git Reference](https://marklodato.github.io/visual-git-guide/index-en.html)

#### 
___

### `Setup/Config`

#### [Git config documentation](https://www.git-scm.com/docs/git-config)

#### `git config --global user.name "[firstname lastname]"`

* Set a name that is identifiable for credit within version history review.

#### `git config --global user.email "[valid-email]"`

* Set an email address that will be associated with each history marker.

#### `git config --global color.ui auto`

* Set automatic command line coloring for Git for easy reviewing.

#### `git init <directory>`

* Create empty Git repo in specified directory.
* `git init` without directory will initialize the current directory as git repository.

#### `git clone <repo>`

* Clone repo located at <\repo> onto local machine.
* Original repo can be located on the local filesystem or on a remote machine via HTTP or SSH.
* Eg. cloning repo from GitHub, the original repo is on remote machine.

___

### `Stage & Snapshot`

#### `git add <directory>`

* Define author name to be used for all commits in current repo.
* Devs commonly use `--global` flag to set config options for current user.
* [git-scm.com/docs/git-add](https://www.git-scm.com/docs/git-add)

#### `git commit -m <message>`

* Commit the staged snapshot.
* With `<message>` one can avoid opening text editor and typing commit message.
* [git-scm.com/docs/git-commit](https://www.git-scm.com/docs/git-commit)

#### `git status`

* List which files are staged, unstaged, and untracked.
* [git-scm.com/docs/git-status](https://www.git-scm.com/docs/git-status)

#### `git log`

* Display the entire commit history using the default format.
* [git-scm.com/docs/git-log](https://www.git-scm.com/docs/git-log)

#### `git diff`

* In overall, show changes between commits, commit and working tree, etc
* Show unstaged changes between your index and working directory.
* In other words, the differences are what you could tell Git to further add to the index but you still haven’t.
* [git-scm.com/docs/git-diff](https://www.git-scm.com/docs/git-diff)

___

### `Undoing Changes`

#### `git revert <commit>`

* Create new commit that undoes all of the changes made in `<commit>`, then apply it to the current branch.
* [git-scm.com/docs/git-revert](https://www.git-scm.com/docs/git-revert)

> One can choose commit, undo current changes and apply selected commit changes to current working branch.?

#### `git reset <file>`

* Remove `<file>` from the staging area, but leave the working directory unchanged. This unstages a file without overwriting any changes.
* [git-scm.com/docs/git-reset](https://www.git-scm.com/docs/git-reset)

> What if though file is imported eg. within other file and used, eg. Javascript project. I guess Git does not pardon my language, dont give a duck about that.

#### `git clean -n`

* Shows which files would be removed from working directory.
* Use the `-f` flag in place of the `-n` flag to execute the clean.
* [git-scm.com/docs/git-clean](https://www.git-scm.com/docs/git-clean)

___

### `Rewriting Git History`

#### `git commit --amend`

* Replace the last commit with the staged changes and last commit combined.
* Use with nothing stage to edit the last commit's message.
* [git-scm.com/docs/git-commit](https://www.git-scm.com/docs/git-commit)

> Last commit replaced with currently staged changes written afterwards to last commit? Somehow difficult explanation to understand.

#### `git rebase <base>`

* Rebase the current branch onto `<base>`, `<base>` can be:
  * Commit ID
  * Branch name
  * A tag
  * Relative reference to `HEAD`
* [git-scm.com/docs/git-rebase](https://www.git-scm.com/docs/git-rebase)

> Find out more later about using git rebase

#### `git reflog`

* Show a log of changes to the local repository's `HEAD`
* Add `--relative-date` to show date info or `--all` to show all refs.
* [git-scm.com/docs/git-reflog](https://www.git-scm.com/docs/git-reflog)

### `Git Branches`

#### `git branch`

* List all of the branches in your repo
* Add `<branch>` argument to create a new brnach with the name `<branch>`.
* [git-scm.com/docs/git-branch](https://www.git-scm.com/docs/git-branch)

#### `git checkout -b`

* Create and check out a new branch named `<branch>`.
* Drop the `-b` flag to checkout an existing branch.
* [git-scm.com/docs/git-checkout](https://www.git-scm.com/docs/git-checkout)

#### `git merge <branch>`

* In overall, join two or more development histories together
* Merge `<branch>` into the current branch.
  
`Warning: Running git merge with non-trivial uncommitted changes is discouraged: while possible, it may leave you in a state that is hard to back out of in the case of a conflict. - git-scm.com/docs/git-merge`

* [git-scm.com/docs/git-merge](https://www.git-scm.com/docs/git-merge)

___

### `Remote Repositories`

#### `git remote add <name> <url>`

* Create a new connection to a remote repo.
* After adding a remote, you can use `<name>` as a shortcut for `<url>` in other commands.
* [git-scm.com/docs/git-remote](https://www.git-scm.com/docs/git-remote)

#### `git fetch <remote> <branch>`

* Fetches a specific `<branch>`, from the repo.
* Leave off `<branch>` to fetch all remote refs.
* [git-scm.com/docs/git-fetch](https://www.git-scm.com/docs/git-fetch)

#### `git pull <remote>`

* Fetch the specified remote's copy of current branch and immediately merge it into the local copy.
* [git-scm.com/docs/git-pull](https://www.git-scm.com/docs/git-pull)

> I guess one way to always reduce merge conflicts when keeping updated with changes made by team-members on the same branch.

#### `git push <remote> <branch>`

* Push the branch to `<remote>`, along with necessary commits and objects. Creates named branch in the remote repo if it doesn't exist.
* [git-scm.com/docs/git-push](https://www.git-scm.com/docs/git-push)
