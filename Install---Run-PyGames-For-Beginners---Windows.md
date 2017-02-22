#Install / Run PyGames For Beginners - Windows

## Install Python 2.7

    [https://www.python.org/downloads/](https://www.python.org/downloads/)
    Run the file
    Make sure to add python to your path
    Path will look like: `C:\Python27\`

## Editing Path

    Search ‘environment variables’
    Select edit environment variables
    Select path, edit
    Add the new path if it is not there
    ‘;’ between each new path

## Install Pip

    Download pip file : [https://bootstrap.pypa.io/get-pip.py](https://bootstrap.pypa.io/get-pip.py)
    Navigate to folder with the file in command prompt
    Run: `python get-pip.py`
    Make sure to add the python scripts folder to your path
    Will look like: `C:\Python27\Scripts`
    Should be able to run the command 'pip' if all went well

## Install Pygames

    Download .whl file : [http://www.lfd.uci.edu/~gohlke/pythonlibs/#pygame](http://www.lfd.uci.edu/~gohlke/pythonlibs/#pygame)
    Make sure there version matches your python version (cp27 NOT cp34)
    Naviage to folder where it's downloaded
    Run `pip install`
    Example: `pip install pygame-1.9.2-cp27-cp27m-win32.whl`
    If you get ‘not supported wheel’ warning you have the wrong version of pygame
    Here is a good walkthough if needed for installing pygame: [https://www.webucator.com/blog/2015/03/installing-the-windows-64-bit-version-of-pygame/](https://www.webucator.com/blog/2015/03/installing-the-windows-64-bit-version-of-pygame/)

## Running Game

    Navigate to PyCut folder
    Run `python pycut.py`
    Game should launch

This guide courtesy of [Patrick Gormley](http://journeyintofoss.blogspot.com/2016/12/install-run-pygames-guide-for-future.html)