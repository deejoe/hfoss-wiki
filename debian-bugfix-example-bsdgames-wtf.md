
# Debian bugfix example: bsdgames-wtf

## Rationale

So, I know that **bsdgames** is the package name for a collection of small
console-based games, and that it is packaged for Debian and Ubuntu.  Because
these are small programs with few dependencies, they make excellent examples
to work on.

## Finding Debian package details online

If one knows the name for a Debian package, one can look up its web page by
just tacking the package name to the end of the base URL
http://packages.debian.org for example:

 * [packages.debian.org/bsdgames](http://packages.debian.org/bsdgames)

The resulting page shows that the package is available across multiple
versions of Debian.  Let's choose the link for the *testing* version,
codenamed *stretch*:

  * [https://packages.debian.org/buster/bsdgames](https://packages.debian.org/buster/bsdgames)

## Using the Debian package-specific page

Most of what we want from this page, then, is in the right-hand sidebar. We
want to look at two things:

  * The [list of bug reports](https://bugs.debian.org/bsdgames)
  * The [original source](http://http.debian.net/debian/pool/main/b/bsdgames/bsdgames_2.17.orig.tar.gz)

## The package buglist

For many packages, opening the bug reports shows a list of bugs listed by
various categories of severity and categorization.

At the time of this writing (late February 2017) we see dozens of bugs
against bsdgames.  One might read through them to see if there are any that
interest you.  The one that stands out to me as being a potential easy win
is updating the list of acronyms for the program `wtf`, [bug #798185](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=798185) (still open January 2018).

Reading it we see that it has a link into relevant portion of the NetBSD
project's web view of its CVS source code repository.

This should be an easy fix, since all we need to do is replace the Debian version of these files with the newer NetBSD version.


## Fixing the bug

To fix this bug, we will leverage what we are learning and using already in
class, which is GitHub as a place to track and host changes to code bases:

We will 
 
  * make a local directory to hold a working copy of the code  
  * download the source code as an archived and compressed file
  * unpack that file into our working directory
  * initiate a local git repository for tracking the files in that directory
  * make our first commit to that local repository
  * create a GitHub project to host our versions of the code publically
  * add the new, empty GitHub project as a remote in our local repository
  * we will push the locally-tracked code to GitHub
  * we will make our edit to the locally-tracked code
  * we will push our edit to GitHub
  * we will send the Debian bugtracker an email with a link to our publically-hosted commit

In more detail, then:

On a local machine, create a new directory, and then move down into it, eg:

  * `mkdir bsdgames`
  * `cd bsdgames`

Now, let's grab the original source for the package. (It might be that the
debian source packages provide important changes, but in the interest of
keeping this simple, we'll disregard that for now.)

You can download the source however you like, so long as you move it
successfully into your 'bsdgames' directory. I'll use wget here:

  * `wget http://http.debian.net/debian/pool/main/b/bsdgames/bsdgames_2.17.orig.tar.gz`

That should leave you with a copy of the file `bsdgames_2.17.orig.tar.gz`

You can use a variety of methods to unpack this file. Here, I'll use the
`tar` command:

  * `tar xvzf bsdgames_2.17.orig.tar.gz`

That creates and fills out a version-specific subdirectory for the code:

  * `bsdgames_2.17`

which we then descend into

  * `cd bsdgames_2.17`

At this point, we have a copy of the source code as received from upstream,
clean and free from any of our modifications.

This is a good time to start tracking our changes. We'll use `git`. First,
let's make sure we have things squared away locally:

  * `git init`
  * `git add . `
  * `git commit -m "first commit of code as downloaded from https://packages.debian.org/stretch/bsdgames"`

This will be enough to track our changes locally. But we will also want to
be able to communicate them to the Debian package maintainer for inclusion,
and possibly work on them collaboratively with other people.  Eventually, if
all goes well, the changes will be in Debian, so that will meet that goal. 

In the meantime, though, let's put it on GitHub.  _(A more Debian-like way of
doing this would be to put the code on their Alioth code hosting site, but
again, let's use what we know now for starters.)_

So, log on to github and create a new project. You should probably just call
it `bsdgames`.

Back on your home system, in the subdirectory that contains the code, add your GitHub repo as a remote:

  * `git remote add origin https://github.com/yourgithubnamehere/bsdgames`

Then, you should be able to push from your local to the remote with:

  * `git push`

You might need more explicitly to specify:

  * `git push origin master`

You might also need to set your [username and email address](https://help.github.com/articles/setting-your-username-in-git/).

With that done, let's fix the bug!

Recall that the Debian bug report includes a link to a NetBSD web page.

That link leads to [a directory](http://cvsweb.netbsd.org/bsdweb.cgi/src/share/misc/?only_with_tag=MAIN) that includes newer versions of the two acronym files `acronym` and `acronym.comp` used by this package in Debian.

If you go to that directory and then click on, just as an example, `acronym` you aren't taken to the file right away. Instead, you are taken to a list of revisions of that file. At the time of this writing (January 2018) the latest version is 1.264. 

If you [click on that version number](http://cvsweb.netbsd.org/bsdweb.cgi/src/share/misc/acronyms?rev=1.264&content-type=text/x-cvsweb-markup&only_with_tag=MAIN)
you'll be able to see the file contents, along with a download link.

Download those two files and make sure they go into the appropriate places, and that you haven't introduced any additional cruft. 

Using the command:

  * git status

copiously throughout this process is helpful to see what has changed, what
might need to be added and committed to the repository, and what might need
to be deleted.

Once you have the newer files in place, add and commit your changes, then push them to
GitHub.

Navigate to GitHub, navigate through the `commit` portion of the web
interface to find the link to your commit.  Copy the link, then go to the
Debian web page for the bug, find the **reply** button and send an email to
the bug tracker with the link to your fix.  With some luck and good humor on
the part of the package maintainer, your change will be accepted.  If not,
at least you've made a decent good-faith start to providing a patch that
addresses the documentation portion of this bug report.

