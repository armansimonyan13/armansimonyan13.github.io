# Git cheat sheet

```bash
git log --graph
```
# Setting your username in Git

## Setting your Git username for every repository on your computer
- Set a Git username:
```bash
$ git config --global user.name "Mona Lisa"
```
- Confirm that you have set the Git username correctly:
```bash
$ git config --global user.name
> Mona Lisa
```
## Setting your Git username for a single repository
- Set a Git username:
```bash
$ git config user.name "Mona Lisa"
```
- Confirm that you have set the Git username correctly:
```bashh
$ git config user.name
> Mona Lisa
```

# Setting your commit email address in Git

## Setting your email address for every repository on your computer
- Set an email address in Git:
```bashh
$ git config --global user.email "email@example.com"
```
- Confirm that you have set the email address correctly in Git:
```bash
$ git config --global user.email
email@example.com
```

## Setting your email address for a single repository
- Set an email address in Git: 
```bash
$ git config user.email "email@example.com"
```

- Confirm that you have set the email address correctly in Git:
```bash
$ git config user.email
email@example.com
```