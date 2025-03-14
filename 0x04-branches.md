# Branches

Allows us t create separate contexts where we can try new things and try multiple ideas on parallel. 

- What happens on one branch, does not affect other branches.
- In git, we usually work inside a `branch` even if we don't specify it.

## The Master Branch

- In git, default branch is master branch. 

- Treated as the official branch. (Source of Truth).

- In 2020, gitHub renamed the branch from master to main. 

## What is Head?
- pointer that refers to the current location in your repository.
- In git, only one branch can be active.
- Head points to this branch.
- Switching to another branch will make the head to switch to that branch. 

## Viewing Branches 
```js
git branch
```
- The  active branch will have an asterisks (`*`).

## Creating Branches

```js
git branch BRANCH_NAME
```
- It will create a branch but not switch to it. 
```js
git branch chapter1
```

Running the `git branch` command, we will view the new branch created.

## Switching Branches

```js
git switch BRANCH_NAME
```

```js 
git switch chapter1
```
- It will change the active branch from `master` to `chapter1`

To view run `git branch`.


