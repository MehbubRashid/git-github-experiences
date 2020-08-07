<h1>git push Guide</h1>

```bash
git push origin master
```
This command will push your master branch to the remote master branch, no matter which branch you are currently on.

```bash
git push origin my-branch
```
Similarly, this command will push your my-branch to the remote my-branch, no matter which branch you are currently on.

**Note:** If my-branch does not exist in remote, it will create it in remote.
But if my-branch does not exist in local, it will throw an error saying

```bash
error: src refspec my-branch does not match any
```

<h2>What is git push -u origin master</h2>

The -u flag refers to 'set upstream'. Which means the remote master branch will be set as upstream for our local master branch.
So that, we can just use git push,git pull without specifying the remote name and branch name.

This command is usually run only first time.


```bash
git push -u origin branch-name
```

Similarly, this will set upstream remote/branch-name for local/branch-name and then git pull, git push can be directly called.

**Alternative Approach:** [How can I tell a local branch to track a remote branch?](https://www.git-tower.com/learn/git/faq/track-remote-upstream-branch)


# git merge Guide

```
git merge branch-name
``` 
This will merge the branch-name with currently logged-in branch.

```
git merge
```
This will merge the corresponding remote branch with current logged-in branch.
Here, upstream must be set previously using ```git push -u origin branch-name``` command.
