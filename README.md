# GitNotes
A set of my notes regarding Git usage that may be helpful for collaboration

## If new repo

**Make project directory, move into direcory then git init:**

```shell
mkdir myproject
cd myproject
git init
```

**Link to Github or other service:**

```shell
git remote add origin https://github.com/username/myProject.git
```

## If existing repo:

**Clone**

```shell
git clone https://github.com/username/remoteProject.git
```

**Add files**

```shell
touch filename
```

**Check status of files in repo:**

```shell
git status
```

## Publish updates to GitHub or other service:

**Add all files/changes to tracking (1)**

```shell
git add -A
```

**Commit changes to tracking with message (2)**

```shell
git commit -m 'message'
```

**Push changes to remote (3, option 1)**

```shell
git push -u origin main
```

**Push changes to remote (3, option 2 - for collab)**

```shell
git push -u origin featureBranch
```

*Note, if you do `git branch` and `git status` before pushing, then you can always be sure that you're pushing to
the correct location and can simply enter `git push`*

## Working with branches:

*Now a main branch has been established and local/remote have been linked. It is recommended to create a new branch to work on features separate from the main branch that can be merged into it by creating a pull request on main*

**List branches**

```shell
git branch
```

**Create new branch**

```shell
git branch -M newBranch
```

**Switch to new branch or back to other branch**

```shell
git checkout newBranch
```

OR

**Create and Switch to new branch at once (Preferred)**

```shell
git checkout -b newBranch
```

## Retrieving updates from GitHub:

**To fetch all tracked changes from remote to local (1)**

```shell
git fetch
```

OR

```shell
git fetch --all
```

**To rebase feature branch on main branch (2)**

```shell
git rebase origin/main
```

**To actually pull all changes from remote to local (3)**

```shell
git pull
```
