# Merging Branches
- Incorporating things we have done in the destination branch. 

To merge branches:

1. Switch to the branch where you want to merge the current branch. `git switch main`

2. Use the command:

```js
git merge BRANCH_NAME
```

```js
git merge chapter1
```

### Fast Forward Merge Technique:

A scenario where, lets say you have the `main` branch and `chapter1` branch which you are working. 

Bob a developer team, makes changes in the `main` branch.

It creates a situation where during merging, `main` has content that `chapter1` does not have and `chapter1` has content that `main` does not have. 

It common and nothing wrong with it.

Git will perform a 3 way merge.
 - git will open the default text editor.
 - Wait for you to write the commit message.
 - File is closed, git completes the commit.


 ## Merge Conflicts

 When git is unable to reconcile differences between two branches.

 ### When Merge Conflict Occur
 1. Concurrent changes - if two branches have changes to the same line, git can't decide which change to keep.

 2. Conflicting Edits - if one branch edits a file that the other branch deletes, git cannot resolve the conflict.

 3. Diverged Histories - If the histories of the branches have diverged significantly, git cannot resolve the conflict.

 ### Conflict Markers 

 The content from your current HEAD (the branch you are trying to merge content into) is displayed between <<<<<HEAD and ======.

 The content from the branch you are trying to merge from is displayed between ========== and >>>>>>>>>BRANCH_NAME symbols where BRANCH_NAME is the name of the branch you are trying to merge from.

 - If there is a merge conflict, git will notify you in the command line.

 ### How to fix merge conflicts.

 - Open the files with merge conflict.
 - Edit the files to remove the conflict. Decide which branch content you want to keep.
 - Remove the conflict marker in the doc.
 - Add your changes and make a commit. 
 
