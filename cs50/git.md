# Notes from CS50's W1 lecture
>Git

Lets goooo.

I still have yet to master this tool.
- With git, we can 
  - keep track of changes to code.
  - synchronize code between different people.
  - test changes to code without losing the original.
  - revert back to older versions of code.

- First we will work on copying the github repo onto our computer.
  - `git clone <url(.git)>` to download the repo.
  - Let's clone `codewars` onto Desktop
- `touch <file>` to create new file(only in gitbash).
- `git add` to add files which will be committed(files to be tracked). When I enter `git commit`, these staged files will be committed.
- `git status` will tell me the status of branches(whether ahead or behind the master branch) and files.
- Finally, `git push` to push the local changes to master or github repo.
- We can use `git commit -am "message"` to commit all files(shortcut). NO need for `git add .` stage.

### `git pull`
To get the changes on github repo that are not in our local repo.
- `git pull <repo link>` to pull the changes from hub repo.
- This can create `merge conflicts` where two different people modify the same line. 
  - `CONFLICT (content).... ERROR MESSAGE` will be displayed.
  - `<<<<` represents my changes 
  - `====` represents remote repo's changes.
- *`git fetch` will fetch the metadata from the reomte repo to see if there are any changes available to merge in local repo.*

### Useful commands

1. `git log` 
    - logs the commits
2. `git reset`
    - go back to previous commits
      - `git reset --hard <commit(hashes)>` to go back to certain commit.
      - `git reset --hard origin/master` to go back to the state of master branch?

### Making changes

### Branching
A way of working on differnt parts of the repo at the same time. 
- The `master` branch is the main branch. The other branches are others. We can then merge the code in the new branch to master.
- The `HEAD` points the branch that we're working on.

>For knowing what branch are we working on:
```git
>>>git branch
master *branch1 branch2

* = currently working branch
```
>Starting a new branch and switching to it at the same time:
```git
>>>git checkout -b new_branch

`Switched to a new branch 'new_branch'` will be displayed.
```
Then we can modify the code, commit and it will just be committed to the new branch as long as we are still on that branch.

>Switching to an existing branch
```git
>>>git checkout master
```
and the modified code from the other branch **new_branch** will be gone and the last commit of the branch **master** will remain.

>Merging the code from the new branch to the master branch
```git
>>>git merge new_branch
(currently on main)
```
- when merged, merge conflicts can (commonly)occur.
  - Manually see the changes and solve the conflicts manually.
  - Then commit.

## Additional GitHub features
### Forking a repo
- When we want to contribute to a certain github repo, we can `fork` it to get it into our account.
- Then we can work on it, modify and to add it into the original repo we're contributing to, we can add a `pull request`. And if the repo owner(s) agree and are satisfied with the changes, they will accept/close the pull request.

### Github Pages
- We can host our websites here.(only small ones with HTML,CSS and a little bit of JS).
>Shortcut to instantly supporting `github pages` without having to manually set up github pages:
```git
Start a repo name ending with .github.io:

Example: this-website.dummyken.github.io
```

---
This is it, bye bye bye!




