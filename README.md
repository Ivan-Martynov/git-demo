# Demo Git Repository

## First commands.

git version
Self explanatory

git status
Showing current status of the repo we are in. Should be run first before
initializing a new repository, because it would confirm whether we are already
inside a repo.

git init
Create a new repository. Never run inside another repo, otherwise problems will
surely emerge at one point or another. If a repo has been initialized inside
another repo by mistake, then we can simply remove the wrong '.git' directory.

git add
Add/stage files for a commit (git add file1.txt file2.txt). Calling
'git add .' will add all modified and new files/folders. Character '.'
represents the current directory.

git commit
Commits the changes to the repository. Updates the '.git' directory.
Requires a commit message, summarizing the changes (git commit -m "message").
Command 'git commit --amend' allows to redo the most recent commit.
Command 'git commit -a -m message' will stage changes and commit.

git log
Logs of the commits.

## Branching

git branch
View existing branches.

git branch branch-name
Creates a new branch (doesn't switch to the branch) based upon the current
HEAD (which point to the most recent commit on the active/chosen branch).

git branch -d branch-name
Delete a branch which must be committed and fully merged.
Using with '-D' option instead of '-d' will force deleting the branch
regardless of its status.

git branch -m branch-new-name
Rename a branch.

git switch branch-name
Switch to a branch. Using with option '-c' it will create a new branch and
switch to it (git switch -c new-branch-name).

git checkout branch-name
Historically, this command was used to switch branches. Better to use switch.

## Merging

git merge branch-name
Merge changes from a specific branch into the current branch.

## Cloning

git clone repo-url
Clone/download a repository.

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

git stash drop stash_id
Remove the stash with a given id.

git stash clear
Remove all stashes.

## Undoing changes

git checkout commit_id
Checkout to a particular commit.

git checkout HEAD~1
Refer to one commit prior the HEAD. Instead of number 1 the user can use other
values to represent a commit prior the HEAD.

### Description

This is the first file in this repo.

Files:

1. Index.html

### Ipsum Below

Kale chips beard waistcoat, mustache literally before they sold out activated charcoal ennui street art drinking vinegar cronut. Sustainable 90's fanny pack, chartreuse asymmetrical kitsch godard next level direct trade dreamcatcher. Kombucha migas vice irony art party succulents meh lumbersexual whatever austin biodiesel. Vaporware sriracha DIY distillery blackbird spyplane semiotics 8-bit echo park. Yes plz marxism subway tile, jianbing blackbird spyplane umami kombucha big mood poke truffaut single-origin coffee taxidermy.

Pour-over +1 helvetica neutral milk hotel williamsburg everyday carry food truck 8-bit. Af tumeric solarpunk locavore intelligentsia pork belly. Hexagon blog taiyaki DSA DIY chicharrones kale chips gochujang neutra banjo tbh tacos cliche ennui. Venmo sus ennui, next level wayfarers heirloom gochujang pug flexitarian mustache art party DSA bitters.

Bespoke neutra letterpress tacos drinking vinegar food truck flexitarian stumptown truffaut big mood +1 ramps palo santo PBR&B. Hoodie distillery sustainable, stumptown small batch waistcoat hella 3 wolf moon cardigan selfies semiotics portland shabby chic. Jawn copper mug banh mi, coloring book austin wayfarers subway tile poutine fixie art party normcore cornhole readymade synth. Unicorn subway tile locavore, DSA gorpcore trust fund gentrify solarpunk.

Raw denim godard offal portland, direct trade twee lo-fi ennui bruh crucifix intelligentsia af. Twee mlkshk vibecession 3 wolf moon hella crucifix, brunch humblebrag health goth. Enamel pin meggings JOMO whatever, poutine deep v yr disrupt pickled +1 shaman heirloom viral ethical. Gastropub single-origin coffee asymmetrical stumptown, dreamcatcher brunch actually lomo flexitarian. Yes plz JOMO cardigan shaman hot chicken photo booth. Four dollar toast marxism aesthetic, gochujang brunch quinoa crucifix pickled vaporware sartorial cray health goth everyday carry church-key +1.
