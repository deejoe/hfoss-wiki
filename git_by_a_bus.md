
First, let's make a subdirectory to contain everything:

    mkdir gbab
    cd gbab

We are using a [previous student's fork](https://github.com/ry60003333/git_by_a_bus) of [the original git_by_a_bus repo](https://github.com/tomheon/git_by_a_bus).

    git clone https://github.com/ry60003333/git_by_a_bus
    cd git_by_a_bus
    git fetch origin v2
    git checkout v2

On *saskia* things work pretty smoothly from here. First, let's put a little distance between ourselves and the git-by-a-bus code for now. 

We'll move up a diretory and then make a virtual environment:

    cd ..
    virtualenv venv

If virtualenv isn't installed, that's fine, we can do:

    pip install virtualenv

or possibly

    pip install --user virtualenv

or if desparate

    python -m pip install --user virtualenv 

(*this latter approach seems to be necessary on Windows 10*)

and then try to make the virtual environment by repeating the command from above again:

    virtualenv venv

We activate the virtual environment with:

    source venv/bin/activate

(Note: the prompt should change to indicate the name of the virtual environment you're in, in this case *venv*).

Now, we go ahead and install `pygments`

    pip install pygments

As per the README there are also dependencies on `nose` and `wsgiref` but these are apparently already installed and the versions available on *saskia* seemed sufficient for it to Just Work.

So far, so good.

Now, let's grab the project we're going to analyze.

Let's use:

    [https://github.com/FOSSRIT/sugar-quickstart](https://github.com/FOSSRIT/sugar-quickstart)

    git clone https://github.com/FOSSRIT/sugar-quickstart

and now let's run GBAB on it:

    python git_by_a_bus/gbab.py sugar-quickstart

This should run for a while, generating a directory called `output`, and then populating it with analysis results.


On the Windows 10 lab machines, we have not yet gotten it to run. The
installed Python 3.6.0 environment offers some challenges, not the least of
which is it not being in the default PATH, requiring something like:

    set PATH=%PATH%;"c:\Program Files (x86)\Python36-32"

or searching for PATH to find the Windows setting for extending the PATH as above.

Additionally, even though (git for Windows)[https://git-scm.com/downloads] is installed, it also seems not to be in the PATH.

Git-by-a-bus offers an option to specify the path to the git executable:

    python gbab.py --git-exe="C:\Program Files\Git\cmd\git.exe" d:\Profiles\djaigm\gbab\git_by_a_bus

For another take on running Python on Windows for HFOSS, see this
(guide to installing Python and PyGame)[Install---Run-PyGames-For-Beginners---Windows]


