# First Flight

The purpose of this homework assignment is to introduce students to their
first FLOSS practices.  Read it in full, there are a number of graded
deliverables.

The due-date is listed in the schedule.

First Flight comes in three phases:

  * Setup: You will create accounts, or identify existing accounts, for the services enumerated below, configure any necessary settings, and begin learning to use them.
  * Reporting: You will gather information about your accounts into a file and then use git to submit that file for inclusion in the course web site.
  * Use: You will use these systems and methods for class communications, including submitting assignments.

## IRC

There is an [IRC](IRC) channel on irc.freenode.net for this course, called #rit-foss. 
[Join this channel and use it](irc-exercise) whenever you can. Communicating regularly in IRC factors into the FOSS Dev Practices 
(daily) component of your final grade.

IRC is one of the primary means of communication for a FOSS community,
particularly for informal communication.

### Tasks:

  * Download and install an IRC client on your development machine.
    * Windows:
      * [HexChat](https://hexchat.github.io/)
    * Mac OS X:
      * [Colloquy](http://colloquy.info/)
      * [LimeChat](http://limechat.net/mac/)
    * Linux:
      * [weechat (console)](https://weechat.org/)
      * [irssi (console)](http://irssi.org/)
      * [HexChat](http://hexchat.github.io/)
    * Web:
      * [IRCCloud](https://www.irccloud.com/) ([SaaSS](https://www.gnu.org/philosophy/who-does-that-server-really-serve.html))
      * [Kiwi IRC (self-hostable](https://kiwiirc.com/)
      * [qwebirc (self-hostable)](https://qwebirc.org/)
  * Choose a nick and [register yourself with the NickServ](http://freenode.net/kb/answer/registration).
  * Connect to #rit-foss on irc.freenode.net and introduce yourself.
    + The instructor’s nick is dzho.

It is a good practice to “hang out” in IRC channels of projects that
you use and especially of projects that you contribute to. Here you can
find early alerts regarding any upcoming major changes or security
vulnerabilities. It is also the easiest (lowest overhead) method for
getting your questions answered.

####   Note

Only for the brave – if you want to be completely awesome, you can
setup a proxy node so you are always logged in. People can leave you
messages this way.

If you want to be completely completely awesome, you can setup
BitlBee so you can tweet or use XMPP from your IRC client 

If you want to be completely completely awesome, you can use Matrix so
you can use IRC when you have intermittent connectivity (as with a mobile
device).


## Email: Mailman

For this course, we use the [floss-seminar discussion mailing list](https://lists.rit.edu/mailman/listinfo.mmcgi/floss-seminar). 
Please subscribe, as part of this exercise.

Discussion mailing lists are a more formal mechanism of communication
for FOSS projects. More formal than IRC, less formal than bug trackers.
Discussion mailing lists are often used to ask questions, announce
upcoming releases and beta tests, and to debate redesigns and
refactors. The advantage here is that mailing lists are typically
archived and indexed by Google; discussions that should be preserved
for posterity should occur here. Upstream projects usually have an
existing mailing list where messages of these sort are to be posted.


## Blogging

You must create a blog (if you don’t have one already) and write at
least one post per week about your progress, attempts, successes,
failures, reflections, and/or all of the above.

Much like mailing lists, blogs are archived, indexed by search engines like
Google and archivers like the Wayback Machine, and therefore can be
preserved for posterity.  When you encounter a technical challenge,
typically you google for a solution and you typically find that solution in
a blog post of some developer who has run into a similar situation. 
Blogging about your attempts, successes and failures (and writing
tutorials!) is a best practice for increasing the general body of searchable
knowledge available, for increasing the [Wisdom of the Ancients](http://xkcd.com/979/).

Blogs around a topic are also typically aggregated by a planet (an RSS
feed aggregator). This way, all developers blogging about Project X can
have their blog posts fast-tracked to a readership subscribed to Planet
X. For instance, here’s a link to [13]Planet Python.

Once all the blog URLs are in hand, the Planet for the course can be hosted at
[http://people.rit.edu/djaigm/planet/hfoss](http://people.rit.edu/djaigm/planet/hfoss)

### Tasks:

  1. Create a blog if you don’t already have one. There are lots of free
     services available. You might try [Wordpress.com](http://wordpress.com) or
     [GitHub Pages](https://github.com/blog/272-github-pages) or
     [Ghost](https://ghost.org/).
  2. Write an introductory post, detailing the process you went through
     to complete the FirstFlight assignment.

#### Note

   Attention Wordpress Users! By default Wordpress will limit the number
   of posts that are listed in the RSS feed to 10. This will create an
   issue roughly halfway through the term when you are supposed to have
   more than 10 blog posts. In order to fix this issue you must take the
   following steps.

    1. Log in to your Wordpress Administration Site
    2. Go to Settings
    3. Go to Reading
    4. Set "Syndication feeds show the most recent"

## Forge: Github

   Code forges are service sites around which FOSS development orbits,
   some of the more popular sites are github, bitbucket, sourceforge, and
   launchpad.

   For your own enlightenment, review the following comparisons of the
   different forges:

  * [Timeline](http://flossmole.org/content/when-were-forges-established)
  * [Metadata](http://flossmole.org/content/project-metadata-matrix-june-2011)
  * [Artifacts](http://flossmole.org/content/artifacts-matrix-code-forges-june-2011)
  * [Features](http://flossmole.org/content/feature-matrix-code-forges-june-2011)
  * [Revision control](http://flossmole.org/content/revision-control-matrix-june-2011)
  * [Policies](http://flossmole.org/content/forge-policy-matrix-june-2011)

   You’ll need to create your own account on github.com.  All development
   for this course should be tracked on that forge by default.  If you'd
   like to incorporate use of a second forge, perhaps one that avoids [particular problems](https://www.fsf.org/news/gnu-releases-ethical-evaluations-of-code-hosting-services), that is an advanced option we
   can discuss.  RIT has a [GitLab instance](https://kgcoe-git.rit.edu), for example.

#### Tasks:

   1. Create a [Github](https://github.com) account if you don’t already have one.

##### Upload an Avatar

   This is **optional** (but appreciated). Humans identify with faces more
   than they do nicknames (surprise!), so go ahead and associate an avatar
   that'll automatically show up in GitHub, the course web site, and other
   places around the web.

##### Gravatar

   Gravatar is now owned by Automattic, who also make WordPress. Go to
   [their site](https://gravatar.com/) and create a WordPress account (or use one you have
   already) and make sure your chosen email address is in there.

#### Libravatar

   [Libravatar](https://www.libravatar.org/) is a free equivalent to Gravatar and has the advantage
   of not requiring a WordPress.com account. Head over to their [New Account page](https://www.libravatar.org/account/new/) and link up your email address with a picture.

#### Patch the Course Project

   Check out the source repository for this course; it’s hosted at
   https://github.com/ritjoe/hfoss.

   Inside the repository, we’ll keep an index of all the students in the
   course and metadata about them (you!).

Tasks:

  * Load up one of the git cheatsheets, copies of which are in [the hfoss-library](https://github.com/ritjoe/hfoss-library): [krueger](https://jan-krueger.net/git-cheat-sheet-extended-edition/) [hbons](https://github.com/hbons/git-cheat-sheet)
  * Work through this [git tutorial](http://gitimmersion.com/index.html) or this [interactive example](https://try.github.io/)
    if you don’t have any experience with git.
  * Fork [the repository](https://github.com/ritjoe/hfoss) ([link to github help](https://help.github.com/articles/fork-a-repo/) on this).
  * Clone a local copy.
  * Add a file in the /ofcourse-content/people/$YEAR/$TERM folder titled
    $YOUR_IRC_NICK.yaml. Perhaps obviously, it is a [YAML file](http://www.yaml.org/). You
    can use the jflory7.yaml file as an example. You will want to make
    sure that you have $TERM in all lowercase. For example a student in
    HFOSS fall of 2014 would have their YAML file in the
    /ofcourse-content/people/2014/fall folder.
    BE WARNED: Your .yaml file must match the format *exactly* (meaning
    it is case and whitespace sensitive.)
  * Once you've confirmed your .yaml file matches exactly, commit and
    push your changes to github, and issue a pull request.
  * Once the patch is accepted upstream and pushed to production, this
    should add your blog feed to the [Participants page](http://hfoss.rocfoss.org/participants).

