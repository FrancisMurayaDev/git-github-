# Stashing


Working in a branch, want to switch to another without committing the latest changes.

We `stash` the uncommitted changes so that we can return to them later without making unnecessary commits.

Stash the changes and come back later to them.

Command:

```js
git stash
```
or 
```js
git stash save
```

Switching back to your branch, you will not see the stashed changes, to bring it back use:

```js 
git stash pop
```

#### You can stash multiple items.
To view what is in the command use:

```js
git stash list
```

To apply a specific stash:

```js
git stash apply stash@{ID}
```
IF its stash id number 3.

```JS
git stash apply stashID@{3}
```

### Deleting a Stash

```js
git stash drop stashID@{3}
```


### Deleting Everything From the Stash

```js
git stash clear
```

