# Logging In To *saskia* Using An SSH Key

  * [Preliminary: Make a new, good passphrase ](#passphrase)
  * [Introduction ](#intro)
  * [Generating a keypair ](#gen-keypair)
  * [Distributing your public key in an accountable way ](#distribute-key)
  * [Using your keypair to connect to _saskia_ ](#connect)
  * [Rationale ](#rationale)
  * [Selected references ](#ref)

## Preliminary: Make a new, good passphrase <a name="passphrase"/>

Prior to completing this key generation exercise, please create and have at hand a good passphrase.

For discussion and tips on generating good, and possibly memorable,
passphrases, see:

[https://www.eff.org/dice](https://www.eff.org/dice)

there is also a pointer there on the use of password managers.

## Introduction <a name="intro"/>

For this exercise, in brief, you will:

  * Log in to _vision.main.ad.rit.edu_ using PuTTY or the ssh command from within git bash.
  * Create an ssh asymmetric public key encryption keypair (aka "an _ssh key_") on _vision_.
  * Copy the public part of the keypair from _vision_ and send to me in IRC by private message (IM).
  * Copy the public part of the keypair to your public web space on people.rit.edu.

We'll be logging in to two machines. We've already logged into _vision_ several times:

`
    vision.main.ad.rit.edu
`

We will, once again, log in to _vision_. That's where you'll enter commands to generate a keypair. The keypair will consist of two files, one of which stays on _vision_ and is protected by your new passphrase. The other you will copy and send to me. 

One of the files is, by default, called ```id_rsa```. This is your *private key*. It should remain on _vision_ and be used only when logged in to _vision_. You should not copy it to anywhere else, and you should not reveal it to anyone else anywhere else in any way whatsoever. That's why we call it *private*.

The other of the two files is, by default, called ```id_rsa.pub```. This is your *public key*. It is meant for being distributed. The security surrounding use of this file is the concern of anyone to whom you give the key. That person has to ask "does this key belong to whom I think it does?" and "if so, do I want to give that person access to a computer I manage?". 

(You don't have to worry about this next part, because if you successfully complete all other steps, it will be done for you: Your public key will be installed by the instructor in a subdirectory of your new home directory on _saskia.igm.rit.edu_. This subdirectory is ```~/.ssh/``` and the file into which your public key will be installed is called ```~/.ssh/authorized_keys```.)

We will be copying your public key file to the system:

`
    banjo.rit.edu
`

We have not used _banjo_ for this class before now. It hosts material for a public RIT web server known as _people.rit.edu_. Another alias for _banjo_ is _gibson_.

We can use programs like FileZilla to copy files to _banjo_ but in this case we will be using the Secure Copy program, ```scp``` from _vision_.

## Generating a keypair <a name="gen-keypair"/>

Please complete the following steps over an on-campus Internet connection (or via the [RIT VPN](https://www.rit.edu/its/services/network-communication/vpn)) using an ssh
client like *PuTTY* or git bash's ```ssh```.


Log in to _vision_ with *PuTTY*, as we've done in class already, or with *git bash*. 

To log in with *PuTTY*, find it in the Windows menu or search for it, open it up and put in _vision.main.ad.rit.edu_ in the dialogue box for the host. 

To log in with *git bash*, find it in the Windows menu or search for it, open it, and at the dollar sign ($) prompt, type in the command:

`
   ssh vision.main.ad.rit.edu
`

Then, when prompted for a username, give _vision_ your [RIT Computer Account](https://start.rit.edu) 
user name.  Once that's entered, you should
get a password prompt.  At the password prompt, please enter the
corresponding password for your RIT Computer Account.

Once logged in, issue the command

`
    ssh-keygen
`

It will ask you for a filename. Please hit return to accept the default
filename, that will make things easier. (it will actually be two filenames,
`id_rsa` which is the private part of the keypair, and `id_rsa.pub` which is the
public part of the keypair).

It will also ask you for a passphrase. Please use a good, unique passphrase
here, not one you've used anywhere else.  A six-word phrase generated as
discussed in the links above would be good.  As is usual when setting a
password or passphrase, you will have to enter it once, then enter it again
to confirm.

As you enter the passphrase, it will appear nothing is happening, there will
be no dots echoed to indicate a character has been entered.  But your
keystrokes will be noted, so please try to keep track of where you are in
entering your phrase.  You may have to start over.

Once you have entered and confirmed your passphrase and the key has been
generated, some information about it will be displayed to your screen,
including a fingerprint hash and a little picture.  These can be redisplayed
at any time using

`
    ssh-keygen -l -f ~/.ssh/id_rsa.pub
`

so no need to make special note of them now.

Once that's done, you can display your public key with:

`
    cat ~/.ssh/id_rsa.pub
`

(if you are in your home directory, you might be able to just issue

`
    cat .ssh/id_rsa.pub
`
)

Once your keypair has been created on _vision_ you are then ready to send the public part of the keypair to your instructor.

## Distributing your public key in an accountable way <a name="distribute-key"/>

There are two relatively simple ways for me to get the public half of your keypair while knowing it is yours. We'll try to do both. One will use IRC, one will use the secure copy (scp) program and the RIT "people" web server.

Then, you can highlight that string by left-clicking and dragging across it.
The public key is about 350 characters long, and should start with 'ssh-rsa'
and then end with something like `dce6789@vision` Please include both the
initial and ending strings with your key, they are part of it.

Then, go into IRC, open a private message session with me by typing
something like:

    `/msg dzho Here is my public key:`

and then paste the key in with a right click. If you make a mistake and post
this publically, it's ok! That's why this is called a *public key*.

The other way I'll have you make the key available to me is to have you
upload it to the public web using the webhost `banjo.rit.edu`.

While still logged in to _vision_ via *PuTTY* or *git bash* `ssh` type

`
 scp ~/.ssh/id_rsa.pub dce5678@banjo.rit.edu:www/
`

but please be sure to use your own RIT Computer Account name in place of the
example placeholder here, *dce5678*.

You will have to enter your RIT Computer Account username and password at
the prompts that `banjo` presents to you.


`
    https://people.rit.edu/dce5678/id_rsa.pub
`

(Again, *dce5678* here is an example RIT Computer Account name only. The
real URL will have your RIT Computer Account name in it.)

When you issue the command, if this is your first time connecting, it will
ask you to accept _banjo_'s public key:

`
    The authenticity of host 'banjo.rit.edu (129.21.17.234)' can't be established.
    ECDSA key fingerprint is SHA256:vjyc+oCEzpVx9OuxHc6zyJDWeHxxFXhOpq3B2tDqzgw.
    Are you sure you want to continue connecting (yes/no)? 
`

(I think everyone will be able to access _banjo_, and that a www subdirectory
will already be on it and working.

If not, we may have to create them by logging in with PuTTY or gitbash ssh, and then issuing:

`
    mkdir ~/www
    chmod a+rx www
`

The first command creates the directory, the second command helps insure its
contents can be read.)


When all is in place, you should be able to type into a browser the URL as
above (but using your own account name in place of dce5678) and should be
able to see your public key.

## Using your keypair to connect to _saskia_ <a name="connect"/>

With your public key in hand, I will attempt to install it for you on the host

`
    saskia.igm.rit.edu
`

on which I have already created for you a (password-disabled) account. When
all is in place, you will first be sure you are logged in to _vision_ as
above. Then, enter 

`
    ssh saskia.igm.rit.edu
`

You will be prompted for the passphrase you created for your key.  As
before, when you enter it, it will not be echoed back to you, nor will any
placeholder characters be displayed to indicate how many characters you have
entered.  Just do your best to enter your passphrase.  If it doesn't work,
try again.  If after several tries you have no luck getting in to _saskia_
please let me know, providing as many details as you can what error messages
you see and about any steps you had problems with.

Once you successfully log in to _saskia_ you should see a prompt similar to
what you've seen already on _vision_, something like:

`
    dce5678@saskia:~
`

(again, with your RIT Computer Account name in place of the example
_dce5678_ used here.)

You can issue the command `exit` at this point and report success, or,
before doing so, explore a bit using the basic commands `ls`, `pwd`, and
`cd`.

 

## Rationale <a name="rationale"/>

I have more control over your account on _saskia_ and so will more easily be
able to do collaborative things with you there than on _banjo_ or _vision_. 

This key creation and distribution process also gives us some practice in
working among different remote hosts, and provides us some practical
experience with asymmetric public key encryption which is both of practical
use and helps inform future discussion of FOSS and computer security.

## Selected references <a name="refs">

  * [PuTTY, a Windows SSH GUI](http://www.chiark.greenend.org.uk/~sgtatham/putty/)
  * [Seahorse, a GNOME SSH GUI](https://wiki.debian.org/Seahorse)
  * [Open source SSH clients](https://fedoramagazine.org/open-source-ssh-clients/) *Fedora Magazine*, Eduard Lucena 
  * [OpenSSH manual pages](https://www.openssh.com/manual.html)
  * [Secure Shell Wikipedia page](https://en.wikipedia.org/wiki/Secure_Shell)
  * [OpenSSH Wikipedia page](https://en.wikipedia.org/wiki/OpenSSH)
  * [RFC4251 The Secure Shell (SSH) Protocol Architecture](https://tools.ietf.org/html/rfc4251)
  * [RFC4252 The Secure Shell (SSH) Authentication Protocol](https://tools.ietf.org/html/rfc4252)



