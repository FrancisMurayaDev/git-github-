# GitHub
Hosting platform for git repositories.
- we put git repos on GitHub and share them across the world. 

Why use GitHub:
1. Collaboration
2. Contribution to open source projects.
3. Exposure to showcase your projects.
4. Staying up to date with trends.


## Cloning GitHub Repos
- getting a local copy of an existing repo hosted on github. 

- We only need the repo URL and tell git to clone it for us.

We use:

```js
git clone URL
```

```js
git clone https://github.com/poteto/hiring-without-whiteboards
```

- git will retrieve all the files associated with the repo and will copy them to your local machine.
-  it initializes a new repo in your machine, giving you access to the full git history of the cloned project.


## Creating a GitHub Account

visit <link>https://github.com/</link> and create an account.


## Getting your project to GitHub.
1. Create a repo in GitHub, connect to our local repo, push changes to GitHub.

2. Create a brand new repo in GitHub, clone down to your machine, work on the repo, push changes to GitHub.

### Remote
- It is the destination we push to in GitHub (remote repo).
- A repo is simply a URL.

To view existing remotes of your repo, run the command:
```js
git remote
```

to get more verbose information we can pass `-v` flag.

```js
git remote -v
```
It will display a list of remotes.

If you have not added any remotes, it will not display anything. 

- Each remote has a name (`origin`) and corresponding `URL`.

We create a remote using the command:

```JS
git remote add REMOTE_NAME REMOTE_URL
```

- Standard remote name is `origin`.
- you can name it anything though.

To rename a remote use the command:

```js
git remote rename OLD_NAME NEW_NAME
```

To remove a remote, use: 

```js
git remove remote REMOTE_NAME
```

### Pushing Changes to the remote.

We use `git push` to push changes to the remote. 

```js
git push REMOTE_NAME LOCAL_BRANCH_NAME
```
example:

```js 
git push origin main
```

It will tell git to push the main branch to a remote called origin.

### The `-U` flag in `git push`

- Allows setting of the upstream of the branch we are pushing.

```js
git push -u origin main
```

From here git will remember where the changes from the local main branch should go.

We don't have to use the full command again.

We can run just `git push` and everything will work.
