<h1>git push Guide</h1>

```bash
git push origin master
```
This command will push your master branch to the remote master branch, no matter which branch you are currently on.

```bash
git push origin my-branch
```
Similarly, this command will push your my-branch to the remote my-branch, no matter which branch you are currently on.





<h2>What is git push -u origin master</h2>

The -u flag refers to 'set upstream'. Which means the remote master branch will be set as upstream for our local master branch.
So that, we can just use git push,git pull without specifying the remote name and branch name. Here, the current logged in branch is important. Because while using git push, it will push to the corresponding branch of the upstream of current logged in branch.
