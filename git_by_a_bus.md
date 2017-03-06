
# Using **git by a bus**

  * [Cloning](#cloning)
  * [Fetching and checking out branch **v2**](#fetch-and-checkout-v2)
  * [Using **virtualenv**](#using-virtualenv)
    * [Creating a virtual environment](#create-a-venv)
    * [Activating and using a Python virtual environment](#activate-and-use-a-venv)
    * [Installing a module into the `venv`](#install-a-module-into-venv)
  * [Finally: Analyzing a project with GBAB ](#run-gbab-on-a-project)
  * [Download the project source code](#download-project-source)
  * [Run GBAB](#run-gbab)
  * [A continuing tragedy: Windows, Python, and GBAB](#windows)



Python on Windows 10 poses challenges to runing git-by-a-bus that seem to be less of a problem on GNU/Linux. So, most of this will focus on how to do this on our GNU/Linux host *saskia*. It might also work on *vision* or even *banjo*.

## Cloning <a name="cloning"/>

First, let's make a subdirectory to contain everything:

    mkdir gbab
    cd gbab

We are using a [previous student's fork](https://github.com/ry60003333/git_by_a_bus) of [the original git_by_a_bus repo](https://github.com/tomheon/git_by_a_bus).

    git clone https://github.com/ry60003333/git_by_a_bus
    cd git_by_a_bus

## Fetching and checking out branch **v2** <a name="fetch-and-checkout-v2"/>

Note well, though, that we are using a non-default branch, branch **v2**, which we must fetch and checkout explicitly:

    git fetch origin v2
    git checkout v2

On *saskia* things work pretty smoothly from here. First, let's put a little distance between ourselves and the git-by-a-bus code for now. 
We'll move up one level in the filesystem, just up a directory level:

    cd ..

This allows the following downloads and additions to be managed independently of the git_by_a_bus local repository.

## Using **virtualenv** <a name="using-virtualenv"/>

### Creating a virtual environment <a name="create-a-venv"/>

The first thing we'll do is create and populate a Python `virtual environment` to hold any additional Python modules we might need to download as dependencies for running GBAB.

Usually, it's a simple matter of just running a command like this:

    virtualenv venv

Here **virtualenv** is a Python command, and `venv` is the name of the directory we're trying to create. If the command is successful, the `venv` directory will contain its own independent and internally consistent copy of Python and associated modules.

If **virtualenv** isn't installed, that's fine, we can do:

    pip install virtualenv

or possibly

    pip install --user virtualenv

or if desparate we may need to run it as

    python -m pip install --user virtualenv 

(*this latter approach seems to be necessary on Windows 10*)

and then try again to make the virtual environment by repeating the command from above:

    virtualenv venv

### Activating and using a Python virtual environment <a name="activate-and-use-a-venv"/>

We activate the virtual environment with:

    source venv/bin/activate

(Note: the prompt should change to indicate the name of the virtual environment you're in, in this case *venv*).

(Also note: when finish, you can exit the virtual environment with the **deactivate** command.)

### Installing a module into the `venv` <a name="install-a-module-into-venv"/>

Now, we go ahead and install `pygments`

    pip install pygments

As per the README there are also dependencies on `nose` and `wsgiref` but these are apparently already installed and the versions available on *saskia* seemed sufficient for it to Just Work.

So far, so good.

## Finally: Analyzing a project with GBAB <a name="run-gbab-on-a-project"/>

### Download the project source code <a name="download-project-source"/>

Now, let's grab the project we're going to analyze.

Let's use [https://github.com/FOSSRIT/sugar-quickstart](https://github.com/FOSSRIT/sugar-quickstart):

    git clone https://github.com/FOSSRIT/sugar-quickstart

### Run GBAB <a name="run-gbab"/>

and now let's run GBAB on it:

    python git_by_a_bus/gbab.py sugar-quickstart

This should run for a while, generating a directory called `output`, and then populating it with analysis results.


## A continuing tragedy: Windows, Python, and GBAB <a name="windows"/>

On the Windows 10 lab machines, we have not yet gotten it to run. The
installed Python 3.6.0 environment offers some challenges, not the least of
which is it not being in the default PATH, requiring something like:

    set PATH=%PATH%;"c:\Program Files (x86)\Python36-32"

or searching for PATH to find the Windows setting for extending the PATH as above.

Additionally, even though [git for Windows](https://git-scm.com/downloads) is installed, it also seems not to be in the PATH.

Git-by-a-bus offers an option to specify the path to the git executable:

    python gbab.py --git-exe="C:\Program Files\Git\cmd\git.exe" d:\Profiles\djaigm\gbab\git_by_a_bus

For another take on running Python on Windows for HFOSS, see this
[guide to installing Python and PyGame](Install---Run-PyGames-For-Beginners---Windows)

It includes installing Python 2.7 instead of the Python 3.6.0 already found on the lab machines.

You can install Python 2.7 on the lab machines, but to make it persistent you cannot use the default install options, you must choose the [**install just for me** option](https://www.howtogeek.com/wp-content/uploads/2014/10/Python-6.jpg.pagespeed.ce.GQOmT4laKi.jpg), so that you can choose to install it on the D: drive (or possibly your Z: drive?)

I would also choose to make a new directory to put it in, named something like *Python27* or *Py27* or some such.

You will, naturally, also have to adjust your **PATH** to include this version. Since this lives in your profile persistently you probably won't have to use **--user** when installing additional modules via **pip**.

