## Merging
 - Let's merge two branches where the pointer of one branch points to a commit that is an ancestor of the other branch
 - git merge will result in a *fast-forward*, i.e. it'll just move the branch pointer that's behind up to the other pointer.
 
```
a points to 1
b points to 4
o--1--2--3--4

git checkout a; git merge b

both a,b point to 4

o--1--2--3--4
```
 - But if I do `git checkout b; git merge a`, a is already merged because all of its commits are in b's history

## Tracking branches
 - a branch that has a remote branch associated with it is a tracking branch. foo tracks origin/foo
