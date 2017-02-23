
# Debian bugfix exampel: robotfindskitten

## Rationale 

So, I know that **robotfindskitten** is the package name for a small
console-based game, packaged for Debian and Ubuntu.  Because it is a small,
simple program with few dependencies, it makes an excellent example to work
on.

## Finding Debian package details online

If one knows the name for a Debian package, one can look up its web page by
just tacking the package name to the end of the base URL
http://packages.debian.org for example:

  * [packages.debian.org/robotfindskitten](http://packages.debian.org/robotfindskitten)

The resulting page shows that the package is available across multiple
versions of Debian.  Let's choose the link for the *testing* version,
codenamed *stretch*:

  * [https://packages.debian.org/stretch/robotfindskitten](https://packages.debian.org/stretch/robotfindskitten)

## Using the Debian package-specific page

Most of what we want from this page, then, is in the right-hand sidebar. We
want to look at two things:

  * The [list of bug reports](https://bugs.debian.org/robotfindskitten)
  * The [original source](http://http.debian.net/debian/pool/main/r/robotfindskitten/robotfindskitten_1.7320508.406.orig.tar.gz)

## The package buglist

For many packages, opening the bug reports shows a list of bugs listed by
various categories of severity and categorization.

At the time of this writing (late February 2017) we
see [only one outstanding bug](https://bugs.debian.org/cgi-bin/pkgreport.cgi?pkg=robotfindskitten;dist=unstable#_0_6_4) against the package.

Reading it we see that it has two wishlist-like requests for changes in how
the game behaves as a game ends.  We will not address these.  

The other component of this report is a straightforward documentation bug:
The documentation does not disclose that hitting 'q' is sufficient to quit
the game.

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

  * `mkdir rfk`
  * `cd rfk`

Now, let's grab the original source for the package. (It might be that the
debian source packages provide important changes, but in the interest of
keeping this simple, we'll disregard that for now.)

You can download the source however you like, so long as you move it
successfully into your 'rfk' directory. I'll use wget here:

  * `wget http://http.debian.net/debian/pool/main/r/robotfindskitten/robotfindskitten_1.7320508.406.orig.tar.gz`

That should leave you with a copy of the file `robotfindskitten_1.7320508.406.orig.tar.gz`.

You can use a variety of methods to unpack this file. Here, I'll use the
`tar` command:

  * `tar xvzf robotfindskitten_1.7320508.406.orig.tar.gz`

That creates and fills out a version-specific subdirectory for the code:

  * `robotfindskitten-1.7320508.406`

which we then descend into

  * `cd robotfindskitten-1.7320508.406`

At this point, we have a copy of the source code as received from upstream,
clean and free from any of our modifications.

This is a good time to start tracking our changes. We'll use `git`. First,
let's make sure we have things squared away locally:

  * `git init`
  * `git add . `
  * `git commit -m "first commit of code as downloaded from https://packages.debian.org/stretch/robotfindskitten"`

This will be enough to track our changes locally. But we will also want to
be able to communicated them to the Debian package maintainer for inclusion,
and possibly work on them collaboratively with other people.  Eventually, if
all goes well, the changes will be in Debian, so that will meet that goal. 
In the meantime, though, let's put it on GitHub.  _(A more Debian-like way of
doing this would be to put the code on their Alioth code hosting site, but
again, let's use what we know now for starters.)_

So, log on to github and create a new project. Call it `rfk` or
`robotfindskitten` as suits you.  (_The longer name is probably better, so
that you can avoid a future conflict with the Markov bot you'll train
against all the known recorded public speeches of the late Senator Robert F. 
Kennedy._)

Back on your home system, in the subdirectory that contains the code, add your GitHub repo as a remote:

  * `git remote add origin https://github.com/yourgithubnamehere/robotfindskitten`

Then, you should be able to push from your local to the remote with:

  * `git push`

You might need more explicitly to specify:

  * `git push origin master`

With that done, let's fix the bug!

The bug report notes what is missing, and where. It's in the info file in
the `doc` folder.

Open the file with an editor, navigate to the point at which it talks about
how to quit the game, and add some text noting that hitting `q` does the job
too.

Then, once you've made the edit, commit your change, then push it to GitHub.

Navigate to GitHub, navigate through the `commit` portion of the web
interface to find the link to your commit.  Copy the link, then go to the
Debian web page for the bug, find the **reply** button and send an email to
the bug tracker with the link to your fix.  With some luck and good humor on
the part of the package maintainer, your change will be accepted.  If not,
at least you've made a decent good-faith start to providing a patch that
addresses the documentation portion of this bug report.

