# Note
- This is a note to record how to use git

## create or clone a repo
Only if you have a repo can you do other things in the following steps.
To get a repo, you can use "git init" to create a whole new repo or just use "git clone" to get a existed repo.

```
usage: git clone [<options>] [--] <repo> [<dir>]
e.g. git clone https://github.com/tangcy98/git-training.git

We sometimes use -b to control the branch we are about to clone.
-b, --branch <branch>
e.g. git clone https://github.com/tangcy98/git-training.git -b master
```

## edit the repo
With the repo we have prepared, we can start to work with it.

Firstly, we should have some basic knowledge about the difference among workspace, staging area(index or just stage), local repo and remote repo.

![avatar](imgs/git-command.png "git command")

Workspace: To be intuitively, it's the root folder of your project, which consists of everything under the folder. It's the place where you edit your whole project directly.

Stage: A place to temporarily store the changes you have made. In fact it is just a record file, which contains the info of the files you are about to commit to the repo(.git/index).

Repo(local): There is always a hidden folder under your project called ".git". This is the so called "repository". Now you might find that the stage is just a small part of repo. The local repo stored all the detailed changes in each version. And there is something like a pointer called `HEAD`, which points at the last version you have commited to the repo.

Remote: It is the server that store your repo and project online, which makes it posible for you to build a repo with others.

- git status
git status: Show all changes you've made after your last commit.
There are several posible status: Untracked, Unmodify, Modified and Staged.
Untracked means a dir/file not in the repo. We can use `git add` to turn it into "Staged" status.
Unmodify means unchanged. If we use `git rm`， then it will become "Untracked".
Modified means changed. We can use `git add` to turn it into "Staged" or just use `git checkout` to reget the source file from the repo and drop the changes sp that it will return to "Unmodify".
Staged: Use `git commit` to sync to the repo.

![avatar](imgs/git-status.png "git status")