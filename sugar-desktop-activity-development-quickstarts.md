
# Getting started developing for Sugar

## Use the Terminal Activity

First let's open the Terminal activity:

  * Go into the XO Home View's list mode.
  * Scroll down to the Terminal activity. 
  * Star it so that it later shows up also in ring mode.
  * Start the Terminal activity.

## Install git

Next, let's install git, so we can use it later.

Once in the Terminal activity, first install __git__:

    sudo yum install git

This will take a while since it will need to download the list of available
packages. You may have to respond to a few prompts along the way.

## Download sugar-quickstart source code

Now, we'll download two different bare-bones Sugar activity source code
repositories from github, one from [Liam Middlebrook's](http://github.com/liam-middlebrook/sugar-quickstart) repository, one from
the [FOSSRIT organization](http://github.com/FOSSRIT/sugar-quickstart). 

Because we are using two packages with the same name (that is,
*sugar-quickstart*) we'll need to give each its own subdirectory.

    mkdir liam
    cd liam
    git clone http://github.com/liam-middlebrook/sugar-quickstart

    cd ..
    mkdir fossrit
    cd fossrit
    git clone http://github.com/FOSSRIT/sugar-quickstart

## Using sugar-quickstart

Follow the instructions in the README file of `liam/sugar-quickstart` and
that of `FOSSRIT/sugar-quickstart` to build each activity.

One important difference you should know about before using either
repository is that the FOSSRIT quickstart is, more simply, a Sugar desktop
activity source code repository, populated with the files and directories
required. 

Liam's quickstart, however, *creates* a Sugar desktop activity
source code directory, and populates *that* directory with the requisite
files and directories.

In the end, the activities that result in the build process are themselves
also different from one another.  Allowing one to note the similarities and
differences between them is one point of this assignment.

Follow along with, and then compare and contrast these simple Activities to, the hello world
activity used in the [sugarlabs hello-world desktop activity development example](https://developer.sugarlabs.org/desktop-activity.md.html).

