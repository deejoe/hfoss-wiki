
# Using branches

See also [Git branches in a nutshell](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)

Make liberal use of local branches to get the hang of making and committing
changes, merging from upstream, or merging or rebasing across branches in
your local repository. 

In this class, if you maintain your `master` branch well, it is the best
starting point for new branches, including feature branches for assignment
submissions and experimental branches on which to practice.

## Making branches

First check what branch you are currently on:

    git status

Then, if not already on `master` change to it:

    git checkout master

Then, create your new branch:

    git checkout -b my-experimental-branch

Branches are cheap and easy to make, so get the hang of creating new ones,
trying things out, and destroying any that don't work.

## Removing branches

When finished with a branch, you can delete it with:

    git branch -d branchname

So long as changes from `branchname` have been fully merged upstream or in
HEAD this will quietly succeed.  Otherwise, it will fail with an error to
prevent you from deleting unsaved work.

If you have some dead-end branch containing changes that you do **not** want
to keep, use

    git branch -D branchname

to force the issue. But just be **sure** you don't want stuff from that branch.

If you force delete a branch with -D you force delete your changes in real
life.

## When things go wrong in a branch

Blowing away just a couple of experimental branches in which everything has
gone wrong is **much** better than deleting your entire repository and
starting over.

So long as 

    git status

shows you on an experimental branch, you can bail out in any of a number of
ways.  Bail out of a bad rebase with

    git rebase --abort

Bail out of a bad merge with

    git merge --abort

Or you can use `git reset` in various ways.

So long as you're on an experimental branch and are committed to blowing it
away anyway, you can even go forward and out instead of trying to back up. 
Add all your changes to the branch, then commit them:

    git checkout -b my-horrible-experiment

    [ ... do bad stuff that doesn't work ... ]

    git add bogusfile1 messedupfile.txt nastyconflictinside.md

    git commit -m "these are all horrible"

    git checkout some-clean-branch

    git branch -D my-horrible-experiment

Git doesn't care if you add and commit them only then to delete them.  It
won't judge you, and if you never merge the branch nor push it upstream, no
one else has to know.

