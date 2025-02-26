# Installation and Setup
- Download Git and Install it. <link>https://git-scm.com/download</link>

To confirm whether you have git installed, open terminal, run the command:

```
git --version
```
- Version number returned, git is installed.

### Configuring Basic Information
In Git we don't register an account, but we need to tell git who we are by configuring our name and email address. 

- User Name

```
git config --global user.name "EnterName"
```

- Email Address

```
git config --global user.email "enterEmail"
```

To verify the configuration you have set: 

For name:
```
git config user.name
```

For Email:
```
git config user.email
```

It will return what you set during configuration. 
