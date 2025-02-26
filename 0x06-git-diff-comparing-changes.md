# `git diff` - Comparing Changes.
We can use `git diff` to view changes between:

- commits
- branches
- files
- working directories



`git diff HEAD`

 will show all changes in the working tree since last commit.

 It includes staged and unstaged changes.

 ## Viewing Staged Changes 

 The things that will be included in your commit.

 or the things that have been added in the staging area.

 ```js
 git diff --staged
 ```

 ## Comparing Changes between branches.

 ```js
 git diff main chapter1
 ```
 we can also separate the branch names using 2 periods.

 ```js
 git diff main..chapter1
 ```

 ## Comparing Changes Between Commits

 1. use `git log oneline` to list all the commits.

 2. Copy the hashes of the two commits you want to compare and pass them to the `git diff`.

 ```js
 git diff a871c7e 24c3f04
 ```
 
