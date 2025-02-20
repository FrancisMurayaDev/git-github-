# Fetching and Pulling

## Remote Tracking Branches

- When we clone a repository from GitHub, we will have the branch `eg: master` and we will also have `origin/master branch`.

- The `origin/master branch` is a remote tracking branch - reference to the state of the master branch in the remote.

- we cant move this branches ourselves.

To view the branches:

```js
git branch -r

```

## Checking our remote tracking branches

When we make changes and commit them, the local branch is what gets moved and not the remote tracking branch.

That is the reason we usually come across a message like, "you branch is ahead of origin/master by 1 commit"

- We can travel back to the remote branch locally using:

```js
git switch REMOTE_BRANCH_NAME
```

FOR EXAMPLE:

```js
git switch origin master
```

## Working with remote branches.

When we clone a repository that has multiple branches from GitHub, how do we work with the branches locally?

When we clone the repository and run `git branch`, we only see the master branch.

How do we get to be able to work with other branches??

RUN:

```js
git branch -r
```

we will be able to see all this branches.

Our local repo knows about these branches with local tracking reference, tell you where these branches are, but we cannot see the local branches.

For example::

You can only see origin/chapter1 but you cannot see chapter1.

To create a branch locally to track `origin/chapter1`.
We can use:

```js
git checkout origin/chapter1
```
But that will put us in a detached head, the solution is to use:

```js 
git switch BRANCH_NAME
```

```js
git switch chapter1
```

This will set-up a local branch called `chapter1` which will track the remote branch `origin/chapter1`.

And that is it, we have a local branch `chapter1`.



## git Fetch

`git fetch` takes remote changes and brings them to the local repository. 

- not automatically integrated into out working files.

- It lets you see what others have been working on without merging those changes in your local repo.

```js
git fetch REMOTE
```

```js
git fetch 
```
or

```js 
git fetch origin
```

If we don't specify the remote, it will use `origin` as the default. 


We can also fetch from a specific branch, we have to specify the branch name and origin name.

```js
git fetch REMOTE_NAME BRANCH NAME
```

Assume we have a branch called chapter1 and remote origin.

```js
git fetch origin chapter1
```

## Git Pull

Used to retrieve changes from a remote repository.

Updates the branch head.

```js
git pull origin chapter2
```

