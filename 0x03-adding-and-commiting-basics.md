# Basics of Adding and Committing.
 - A commit - a checkpoint in time, snapshot of changes in the repo.

 Commit process records snapshots of your project at various stages allowing you to:
 - Track progress.
 - Revert Changes.
 - Collaborate with others efficiently. 

 ## Git Repo

 Works place that tracks and manages files within a folder.

 Using git with a project we need to create a repository.

 - A project can only have 1 git repo.

 ### Creating/Initializing a git repo.

 ```
 git init
 ```
 - A git repo is initialized in the project folder.
 - where it will track and manage changes.

 Use:
 ```
 git status
 ```
 to confirm if your project has a git repo or not.

 ### Adding Changes to the Staging Area
 ```
 git add FILE_NAME
 ```
 Example:
 ```
 git add chapter1.txt
 ```

 Add multiple files by listing all of them: 

 ```
 git add chapter1.txt chapter2.txt chapter3.txt
 ```
 Adding all files in one go using `.` or `-A`

 ```
 git add .
 ```
 or
 ```
 git add -A
 ```

 ### Committing Changes 

 A commit has 4 component:
 
 1. A Hash - unique identifier for each commit.
 2. Commit Message - explains purpose of the commit.
 3. Author - person who made the commit.
 4. TimeStamp - Time and date the commit was made.

 - Commit works if there are changes in the staging area.

 ```js
 git commit -m "commit message"
 ```

 Passing:

 ```js
 git commit
 ```
without other options will open a text editor called `Vi` by default for you to type the commit message. 

`vi` is not beginner friendly.

We can configure it to use the text editor of our choice for commit messages.

1. VS Code
```js
git config --global core.editor "code--wait"

```

now when we run git commit, instead of git opening vi, it will open VS code for us to type our comprehensive commit message.
the --wait flag is used to tell git to wait for us to make changes and close vs code before it continues.

2. Note Pad
```js
git config --global core.editor "notepad"
```


### Viewing Past Commits

```
git log
```
To view past commit in a summarized manner we pass the flag `--oneline`.


```
git log  --oneline
```

### Adding and Committing
- Add changes to staging area.
- Committing to git.

We can add and commit using the shortcut:

```js
git commit -m "COMMIT_MESSAGE" FILENAME
```

By listing files:

```js
git commit -m "COMMIT MESSAGE" chapter1.txt chapter2.txt
```
Committing all Files in Working Directory:

```js
git commit -am "COMMIT MESSAGE"
```

### To edit a Previous Commit Message

Editing the most recent commit message:
```js
git commit --amend
```
