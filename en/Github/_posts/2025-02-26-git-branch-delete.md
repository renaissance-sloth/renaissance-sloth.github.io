---
title: "Delete Git branches"
excerpt: 
tags: Github Git branch 
header:
  teaser: https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png
---

Let's learn how to delete branches.

# Local Branches

## Checking Local Branch List

First, check the list of local branches.

```
git branch
```

## Switching Branches

To delete a local branch, you must switch to a branch other than the one you want to delete.

```
git checkout <branch name>
```
This command allows you to switch to the `<branch name>` branch.

Example - Switching to the main branch:
```
git checkout main
```

## Deleting a Local Branch

```
git branch -d <branch name>
```

The `-d` flag is short for `--delete`, indicating deletion.

Example - Deleting the test branch:
```
git branch -d test
```

### Error 1: Currently Checked-Out Branch
You cannot delete the branch you are currently working on.

If you encounter this error:
```
error: Cannot delete branch '<branch name>' checked out at '<repository path>'
```
It means you tried to delete the currently checked-out branch. Refer to the **Switching Branches** section, switch to another branch, and try again.

### Error 2: Unmerged Commits
If the branch you want to delete contains commits not merged into other branches or repositories, Git prevents accidental loss of commit history by throwing an error.

If you encounter this error:
```
error: The branch '<branch name>' is not fully merged.
```
Use `-D` instead of `-d` if you still want to force deletion.

The `-D` flag is short for `--delete --force`, indicating a **force delete**.

# Remote Branches

## Checking Remote Branch List
Check the list of remote branches:
```
git branch -a
```
The `-a` flag (short for `--all`) shows both local and remote branches.

```
git branch -r
```
The `-r` flag (short for `--remotes`) shows only remote branches.

## Deleting a Remote Branch
The default repository name is usually `origin`.
```
git push <remote name> -d <branch name>
```

Example - Deleting the test branch:
```
git push origin -d test
```

### If You Don't Know the Remote Name
```
git remote
```
This command displays the remote repository name.

# Summary
## Listing Branches
- Local: `git branch`
- Remote: `git branch -r`

## Deleting Branches
- Local: `git branch -d <branch name>`
- Remote: `git push <remote name> -d <branch name>`