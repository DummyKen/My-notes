# Notes about git branches from Net Ninja's vid

The original default branch is the **master** branch. When we want to just test out the code which we dont know for sure will work and dont want to mess up the main branch, we create other branches. And then we can merge it to the master branch once 

- `Master` branch is the main and public branch.

>Creating a new branch
```git
git branch feature-1
```
>Branchest list
```git
git branch -a
```
>Switch to a branch
```git 
git checkout feature-1(branch)
```
- The other processes are the same.
- Files from one branch will not get involved with others.

>Deleting a branch
- First switch back to `master`
```git
git checkout master
```
- Delete
  - Use `-d` only after merging the branch(to the master)
  - Use `-D` otherwise.
```git
git branch -d feature-1

git branch -D feature-1
```
#### Work on two branches

>Create a branch and check it out instantly.
```git
git checkout -b feature-a
//created a new branch 'feature-a` and checked into it.
```
