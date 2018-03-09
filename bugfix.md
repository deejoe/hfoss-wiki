# Homework - Bugfix

WAT? Y?
-------

Real learning in computing comes more from **doing** and less from
studying. Debugging, figuring out how some software works and how it
doesn't, is an interactive process that develops basic engineering
practices and, in the open source context, community engagement and
collaboration.

Find a bug
----------

A bug can be anything: an unintended side-effect in a low-level routine,
a user-interface cleanup, a feature enhancement, grammatical errors or
lack of clarity in the project's documentation.

Broadly, you have two different options here. You can:

  * Find a known bug (or feature enhancement) listed in the project's bug tracker.
  * Find a bug yourself by using the software (this may take a while...)

In the event of the second case, make sure you file the bug in the project's tracker before proceeding.)

You can fix a bug in any project you like. The best to pick is something
you *already use*, something with which you're already familiar. If you
can't think of any projects to investigate off the top of your head,
here's a list of suggestions.

  * Check out the "easy-fix" bugs `Listed by the Fedora Project`
  * Look at [Python easy issues](https://bugs.python.org/issue?status=1&@sort=-activity&@dispname=Easy%20issues&@startwith=0&@filter=&@group=priority&@columns=id,activity,title,creator,status&keywords=6&@action=search&@pagesize=50)
  * Use the search function at [GitHub](http://github.com/) and filter by language (to a language that you know).
  * You could even look up some of the bounties (AKA Bugs that you get paid to squash) at [Bountysource](https://www.bountysource.com/trackers).
  * Take a look at [Up For Grabs](http://up-for-grabs.net/)

Really, the sky is the limit here.


Use the Source, Luke
--------------------

Once you've identified a bug that needs fixing, you'll need to get ahold
of the source. In most cases, the code for a project will be hosted on a
forge and the process of forking and cloning the source should be
straightforward. If you forget how to do this for `github`, you can
refer to `Homework - First Flight`.

1.  For whatever project you've chosen, you should ask that project's community for help. Look for **IRC** channels and project mailing lists. You'll be communicating with developers who have a lot on their plate so make sure to `be polite and leave your ego at the door.`
2.  Find the code related to the bug; use whatever code navigation tools you're more familiar with.  decauses's favorite method is: ```$ grep -inr "SOMEKEYWORD" project_src/ .```
3.  Fix the bug, this may require some thinking, and some more asking around.
4.  Test your fix! Project maintainers hate nothing more than receiving a patch that breaks every other function of the project. Often, projects have built-in test suites. If yours does, run it! 
5.  Prepare your patch with descriptive commit messages. Follow the method for submitting patches recommended by your project and submit!
6.  Make sure the project community can easily understand what you did and why you did it.
7.  Make sure there is a reference in the tracked bug ticket to your patch (that is, if the project maintains a bug tracker).

Consider what [How to Contribute to Open Source](https://opensource.guide/how-to-contribute) has to say about the process.

The Deliverable
---------------

Write a blog post about this process and provide relevant links where
possible to documentation.


1.  A link to the patch(es) hosted somewhere on the web, usually forges provide the ability to link to changesets.
2.  A link to any mailing list discussions archived on the web.
3.  Snippets of any relevant IRC conversations.

You will be graded on your post and the explanation of your process.
Extra kudos (but not extra credit) for super epic patches. Extra credit
(actual extra credit) for patches that are actually accepted upstream.

### Submitting the Deliverable

As with **all** of your assignments, you'll be submitting them via your ```.yaml``` file through a pull request on Github. Be sure to follow formatting and whitespace, and to name your entry in the hw directory like so: ```bugfix: http://yourblog.blogplace.com/bugfixpost```.

