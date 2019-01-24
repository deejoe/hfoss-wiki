
# HFOSS IRC Guide

## Freenode

We use [the Freenode network](https://freenode.net) for chat.

Understand that IRC servers can be standalone, or joined into any one of a 
number of networks of geographically dispersed servers across which traffic 
is **relayed** (hence the R in IRC). Server administrators, moderators, 
channel operators, and other participants cooperate to run the networks.

Freenode hosts several RIT-related IRC channels and, largely through the 
coordinated efforts of RIT's Justin Flory (jwf/jflory) and Freenode staff, 
it reserves the namespace #rit for RIT use.

These include 

    #rit-innovation 
    #rit-foss       
    #rit-foss-unregistered 
    #ritlug         
    #rit            
    #ritlug-teleirc 
    #rit-tigeros   
    #rit-foss-admin


Documentation for using IRC on Freenode is split amongst:

* whatever client you use
* inline documentation available from the server via /help
* inline documentation available from services via /msg ServiceName help
* The [Freenode Knowledge Base](https://freenode.net/kb/all)

The following Freenode KB items cover the basics of using Freenode:

* Familiarize yourself with [Freenode's General Expectations for Conduct](https://freenode.net/kb/answer/conduct) which are largely in line with RIT's policies.
* Read about [connecting to freenode](https://freenode.net/kb/answer/chat)
* Once connected, [register your nick](https://freenode.net/kb/answer/registration). You will need to supply an email address to them.
* Review [how Freenode channels work](https://freenode.net/kb/answer/channels) 

You may eventually find these more advanced topics useful

* [Resetting your password](https://freenode.net/kb/answer/sendpass)
* [Channel Guidelines](https://freenode.net/changuide)
* [Connecting with SASL](https://freenode.net/kb/answer/sasl)
* [Channel modes](https://freenode.net/kb/answer/channelmodes)
* [Channel namespaces](https://freenode.net/kb/answer/namespaces)
* [Extbans](https://freenode.net/kb/answer/extbans)
* [User and project cloaks](https://freenode.net/kb/answer/cloaks)
* [User modes](https://freenode.net/kb/answer/usermodes)


**Freenode is a free and open source software community.**  Its emphasis is more
on supporting FOSS developers and users rather than producing software
directly.  As such we might include it in our broader study of FOSS
communities and practices, nothing for instance its stated
[philosopy](https://freenode.net/philosophy) and
[policies](https://freenode.net/policies) and comparing and contrasting to
other FOSS communities.

## Behavioral lore

Beyond the conduct guidelines, policies and documents there are some
cultural things that might help you understand how participating in IRC
works. One significant thing is that the **I** in **IRC** stands for
*Internet*, as opposed to the *Instant* in **IM**. Though you may see a nick
connected to the channel, the person running that connection may be
*idling* and not available to interact immediately. 

If you have something to say to someone whose nick you see connected, go
ahead and **highlight** them by starting your message with their nick.

Depending on how they have their notifications set, if they are attending to
the system on which their client is running, this may alert them to your
message. If they come back to the client later, this will help them find
your message in the **backscroll**.

Please avoid asking if someone is paying attention with a [contentless ping](https://err.no/personal/blog/tech/2006-10-10-12-05_contentless_pings/)

Also, generally speaking, while you are expected to make some effort to "do
your homework" in preparing to ask a question by doing a web search or
capturing relevant error messages or version numbers or the like, you should
avoid **asking to ask**. If you have a well-formed question, please just ask
it. Don't ask to ask, don't ask if anyone can help, don't ask if anyone
knows THIS THING or THAT THING. Just ask your question, and if someone
thinks they can help, they will try.

Most of VM Brasseur's [getting started](https://opensource.com/article/16/6/getting-started-irc) ([archive](https://web.archive.org/web/20180406165513/https://opensource.com/article/16/6/getting-started-irc)) and 
[quickstart](https://opensource.com/article/16/6/irc-quickstart-guide) ([archive](https://web.archive.org/web/20180618173004/https://opensource.com/article/16/6/irc-quickstart-guide)) guides 
to IRC also apply and deserve a good look, too.

## Bots

The interactive behavior associated with some of the nicks in a channel are
not directly guided by a human operator. Rather, these are autonoma,
programs designed to connect to a channel to carry out various tasks, aka
**bots**. (See [IRC bot](https://en.wikipedia.org/wiki/IRC_bot)

Though their full operation is beyond the scope of this document
**NickServ** and **ChanServ** services are effected through bots operated by
Freenode staff.  They are, if you will, bots-with-benefits.

Useful, well-behaved and well-managed bots are generally welcome in
#rit-foss though as in most things consulting with the community and keeping
them informed as to the purpose of your bot is a good idea.  You should
ensure that there is a well-known, out-of-channel means to contact you in
case a bot becomes a problem.  Your bot may be **kicked** or **banned** from
a channel if it becomes noisy or otherwise causes trouble.


### foss_bot

foss_bot is managed by dzho, inherited from decause (whether decause
initiated it or whether he inherited from previous instructors or students
dzho does not, at the time of this writing, know). 

foss_bot's addressing prefix is the exclamation mark, aka *bang*: `!`

foss_bot can be given quotes to store:

`!quote add test of quote goes here along with any attribution or comment`

and it can be directed to retrieve quotes, either randomly:

`!quote random`

or by number, eg:

`!quote #383`

foss_bot tracks karma

foss_bot helps us manage class meetings. As such, it sometimes logs the
channel in a highly visible (though not entirely public) way.

Read more about [using something like foss_bot for meetings](https://fedoraproject.org/wiki/Meeting:Guide).

### Other bots

Other bots include:

#### Mailing list bots

`fm-rit` and `fm-stg-rit` post notifications into the channel whenever
messages are sent to one of the [FOSS@RIT mailing lists](https://lists.fedoraproject.org/archives/list/fossrit@lists.fedorahosted.org/)
hosted by the Fedora Project.

In a way, they resemble a bridge, but are one-way.

#### Giphy

`Giphy[m]` connects through the Matrix bridge to the [Giphy service](https://en.wikipedia.org/wiki/Giphy)

managed by nolski

#### cowsaybot

also managed by xforever1313

When feeling well, will moo out a message as per [Cowsay](https://en.wikipedia.org/wiki/Cowsay)

Try, for instance, something along the lines of:

`!cowsay Hello, world!`

#### fanshawe

Managed by jwf/jflory. Powered by [Limnoria](https://github.com/ProgVal/Limnoria). Config found [here](https://github.com/jwflory/infrastructure/blob/master/roles/irc/limnoria/templates/limnoria-fanshawe.conf).

fanshawe's addressing prefix is a single period: `.duckduckgo Hello world!`

#### xbot1313 

Managed by xforever1313. It is sensitive to ALL CAPS.

#### kettlefish 

bot *emeritus* managed by Qalthos


## Logs and privacy

As with any form of social media, one should exercise some caution in what one posts to IRC.

That said, there is an expectation that any logs made in a channel should
not be published (eg, rendered publically readable) without due
consideration and prominent notice, particularly in the /topic of the
channel.

We do not publish regular, public logs of channel activity. Neither should
you without significant consultation and buy-in from the community.

**NB:** Please do be aware that individuals may be logging activity, that
foss_bot logs the channel during meetings, and that some bridges cache
channel content.


## Bridges

IRC is the chat method used for HFOSS.  

IRC is an old and very deeply established FOSS communications method. Many
chat services have come and gone during its time, and several others are
available today. As with any technology, it has its strengths and
weaknesses. These are valued more or less highly depending by turns on need,
preference, and fashion.

We cooperate with the broader FOSS@RIT community by welcoming the
establishment and maintenance of bridges between IRC and other chat systems,
however.  An HFOSS student is welcome to use whatever bridge on an
as-available basis.  The student may wish to do so particularly if that
student is already using one of the other chat systems.

That said, bridges are available on a best-effort basis by those providing
and managing them. They may come and go. They may carry traffic in only one
direction. They may drop some information. Some features may not be
available from one diretion (eg, the `/names` IRC command only shows
connected IRC clients, and except for Matrix cannot see beyond the bridge as
to who might be connected). They may require the use of a third-party
service for accessing some content (media or long messages in Matrix get
replaced with a link). 

Generally, to address someone on the other side of a bridge, you have to a)
already know their userid on the remote service (this may be available from
backscroll) and b) you must prepend their userid, in GitHub or Twitter
fashion, with the *at* symbol: @

### Use of bridges by HFOSS students

**NB:** *A student is **not** excused from participation in class
activities, exercises, nor assignments requiring IRC due to a problem with a
bridge.* Each student should be prepared to participate through a proper
IRC client when required.

Students may report problems with bridges, but those reports will be treated
as informational and advisory wishlist or wontfix bugs rather than as
blocking bugs.  Students are encouraged to cultivate a working relationship
with the community developing and operating the bridges and to go to that
community for support as they see fit.


### Non-free chat systems

Some bridges and the chat systems to which they connect to IRC are
**end-to-end free**, which is to say, these systems consist entirely of free
and open source software.  These systems and bridges are more in scope as
objects of use and study for the course and may attract additional support
from the instructor.

Some bridges and chat systems are only partially free. Often, the bridge
software or other clients for the other system are free software, but the
server software for the system is not. These systems are tolerated in HFOSS
so that we may better welcome newcomers to FOSS approaches. Your instructor
will thank you though for avoiding encouraging or promoting the use of these
proprietary programs.


## Bridges in #rit-foss

We have bridges for several services, including:

### Matrix 

There now are several clients for Matrix, but the one available through
f-droid.org and for browsers is riot.im. We have so far used the bridge
maintained with the help of Freenode with matrix.org servers.

Bridging with Matrix is done on a per-connection basis. Each connection from
the Matrix side shows up as a separate nick, eg, `dzho[m]`. The `[m]`
postfix is commonly, but not universally or obligatorily, used for such
nicks.

*Matrix is FOSS.*

Read more about [using Matrix](https://opensource.com/article/17/5/introducing-riot-IRC).

### Telegram

`tg-ritfoss` bridges to Telegram. Though many clients and bridges for
Telegram are FOSS, the **Telegram server software is not FOSS**.


### Slack

`slack-ritlug` bridges to Slack. **Generally, Slack is not FOSS.**

### (XMPP)

Though currently no community of FOSS@RIT participants use XMPP
in a coordinated way, [biboumi](https://biboumi.louiz.org/) is available to
allow XMPP clients to bridge to IRC. Implementing this is a wishlist item.

In the other direction, one can connect with an IRC client to an XMPP
server via [bitlbee](https://www.bitlbee.org) 




