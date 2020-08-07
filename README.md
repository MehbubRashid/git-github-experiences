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


## How to review and test the codes of a github pull request locally and merge the pull request

First we have to create a local branch using that pull request. This branch will be representing how it will look if we merge the PR.

```
git fetch upstream pull/37/head:new-branch-name
```

37 is the id number of the pull request in github. This will fetch the output of that PR and save it in our local new-branch-name

Now we can checkout to new-branch-name and test our code.

After we are done testing and checking, we are finally good to merge the PR. We will do it locally too. First we need to merge this new-branch-name with our local master branch. It is always a good idea to ```git pull``` everytime before merging anything to local master.


```
git checkout master
git pull
git merge new-branch-name
```

Now that we have the PR merged in our local master, we will now push it to the remote master.

```
git push origin master
```

Or

```
git push
```

We can now check on github, the PR is merged there too!

## Merge commits VS Merge squash VS Rebase

!(https://i.stack.imgur.com/3GuQE.png)
