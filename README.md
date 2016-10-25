## Merging
 - Let's merge two branches, where the pointer of one branch *a* points to a commit that is an ancestor of the other branch *b* (see ASCII art below)
 - `git merge` will result in a *fast-forward*, i.e. it'll just move the *a* branch pointer that's behind up to the *b* branch pointer.
 
```
a points to 1
b points to 4
o--1--2--3--4

git checkout a; git merge b

both a,b point to 4

o--1--2--3--4
```
 - But if I do `git checkout b; git merge a`, a is already merged because all of its commits are in b's history!

## Tracking branches
 - Tracking branch: a local branch that has a remote branch associated with it. ex. foo tracks origin/foo
 - `git checkout --track origin/branch`

## Rebasing
 - Say you're on "top" branch
 - You have "bottom" branch which diverges from an ancestor commit of "top"
 - You want to move "top" on top of "bottom"
 - `git checkout top; git rebase bottom`
 - or `git rebase bottom top`
 - generally speaking, `git rebase <base branch> <branch to go on top of base>`
 
 [Fork/pull request workflow](https://git-scm.com/book/en/v2/Distributed-Git-Contributing-to-a-Project#Forked-Public-Project)
