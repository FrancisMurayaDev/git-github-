# git tags
In git we can tag/label commits.

We can use tags to mark version releases. 

## 2 Types of Tags:

1. Lightweight tags. -  a name and a label that points to a particular point in time.

2. Annotated tags. - store extra meta data including author name, email, date and tag/commit message.

- Tags are used to version projects.

## Semantic Versions
The system is three numbers with two dots between them:

`3.8.2`

- The right most number `2` represents patch release. Patch releases its just bug fixes and other changes that don't impact the code.

- The middle number `8` represents minor releases. Its new features, functionalities.

- The left number represents a major release. No longer backward compatible. 

### To View Tags:

```js
git tag
```

### Searching tags using a particular pattern.

We pass the -l flag to git tag, then pass PATTERN as string.

For example viewing all tags starting with 17.

```js
git tag -l "17"
```

### Checking out Tags

To look at the state of a repo at a particular tag:

```js
git checkout TAG
```

For example:

```js 
git checkout 17.0.0
```

This will show us how the project/repo at 17.0.0 looks like.

## Creating a Light-Wight Tag

```js
git tag TAG_NAME
```
```js
git tag v1.0.0
```

## Creating annotated tags.

Pass a `-a` to git tag.

```js
git tag -a TAG_NAME
```

## Tagging previous commits

```js
git tag -a TAGNAME COMIT_HASH
```

## Deleting Tags

Pass `-d` flag to `git tag`

```js
git tag -d TAG_NAME
```

## Re-Using a Tag

Reusing a tag can result to an error.

To use pass the `-f` flag in `git tag`.

```js 
git tag TAG_NAME -f
```

```js
git tag v1.0.0 -f
```

## Pushing Tags

When pushing commits, the tags are not pushed.

We pass `--tags` flag.

```js
git push --tags
```
To push a single tag, we specify the remote name and tag-name.

```js
git push origin v1.1.0
```

GitHub will show you how many tags you have.

