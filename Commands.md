## Git commands.

### Version

git version
Self explanatory

### Status

git status
Showing current status of the repo we are in. Should be run first before
initializing a new repository, because it would confirm whether we are already
inside a repo.

### Init

git init
Create a new repository. Never run inside another repo, otherwise problems will
surely emerge at one point or another. If a repo has been initialized inside
another repo by mistake, then we can simply remove the wrong '.git' directory.

### Add

git add
Add/stage files for a commit (git add file1.txt file2.txt). Calling
'git add .' will add all modified and new files/folders. Character '.'
represents the current directory.

### Commit

git commit
Commits the changes to the repository. Updates the '.git' directory.
Requires a commit message, summarizing the changes (git commit -m "message").
Command 'git commit --amend' allows to redo the most recent commit.
Command 'git commit -a -m message' will stage changes and commit.

### Log

git log
Logs of the commits.

## Branching

### Using branch

git branch
View existing local branches.

git branch -r
View remote branches.

git branch branch-name
Creates a new branch (doesn't switch to the branch) based upon the current
HEAD (which point to the most recent commit on the active/chosen branch).

git branch -d branch-name
Delete a branch which must be committed and fully merged.
Using with '-D' option instead of '-d' will force deleting the branch
regardless of its status.

git branch -m branch-new-name
Rename a branch.

### Using switch

git switch branch-name
Switch to a branch. Using with option '-c' it will create a new branch and
switch to it (git switch -c new-branch-name).

### Using checkout

git checkout branch-name
Historically, this command was used to switch branches. Better to use switch.

## Merging

git merge branch-name
Merge changes from a specific branch into the current branch.

## Cloning

### Using clone

git clone repo-url
Clone/download a repository.

### Using remote

git remote
View existing remotes.

git remote add name url
Add a remote with specified name (typically, origin) and the url address.

## Comparing (aka diff)

git diff
Shows changes in the working directory that are not staged.

git diff HEAD
Shows staged and unstaged changes.

## Stashing

git stash
Save changes which are not ready for a commit yet.

git stash pop
Reapply changes from the stash.

git stash apply
Apply stuff from the stash without removing it from the stash.

git stash list
View all stashes.

git stash drop stash-id
Remove the stash with a given id.

git stash clear
Remove all stashes.

## Undoing changes

### Using checkout

git checkout commit-id
Checkout to a particular commit.

git checkout HEAD~1
Refer to one commit prior the HEAD. Instead of number 1 the user can use other
values to represent a commit prior the HEAD.

git checkout HEAD file-name
Revert the file provided by file-name to the state it was at HEAD.
Another way to do the same thing is to call 'git checkout -- file-name' (the
HEAD was replaced with --).

### Using restore

git restore file-name
Restore the file to the contents it had in the HEAD. Basically, it is the same
command as 'git checkout HEAD file-name'.

git restore --source commit-id file-name
Restore the file to the contents according to the specified commit (for
example, HEAD~2 to take the commit second prior the HEAD).

git restore --staged file-name
Remove a file from the staging area. It doesn't delete or modify the file - it
only becomes unstaged.

### Using reset

git reset commit-hash
Reset repository to the specified commit. The working directory will still
contain the changes, but commits after the specified one will be lost.

git reset --hard commit-hash
Hard reset repository to the specified commit. The working directory lose the
changes AND commits after the specified one will be lost.

### Using revert

git revert commit-hash
Creates a new commit with reversed/undid changes. As a new commit, it will
require a commit message.
