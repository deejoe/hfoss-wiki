
Working with an upstream project through a fork of that project usually
requires your working repository to know how to reach two remotes.

When you clone your fork of the repository, your fork starts out as the only
remote for that clone to work with. This remote uses the default name of
"origin". 

You will be able to pull and fetch from "origin" to your working repository.
So long as you have cloned from a repository to which you have write access,
you will also be able to push to it.

You won't be able to push to the original from which you forked, though.
But, you might need to be able to incorporate changes, which is to say, to
track changes, in the original repository if you hope to have any of your
submitted pull requests accepted. If your repositories diverge too much from
the original it will become impractical to include any of your changes.

You could generate pull requests from the original project into your GitHub
fork, and then accept them, all through the web interface. But that is
tedious.

Instead, you can pull (or fetch then merge) from the original repository by
configuring it as an additional remote. The convention is to call this
remote 'upstream'. 

In this course, you have forked from https://github.com/ritjoe/hfoss so to
add that as the remote named 'upstream' in your working repository, issue
the command:

    git remote add upstream https://github.com/ritjoe/hfoss

You can then issue, for instance

    git pull upstream

to bring upstream changes into your repository. 

This approach is generalizable to non-GitHub remotes.

To read about it in the GitHub context, see:

  * https://help.github.com/articles/configuring-a-remote-for-a-fork/
  * https://help.github.com/articles/syncing-a-fork/

