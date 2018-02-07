
# Python virtual environments and pip

## Python versions

```
which python

which python3

python --version

python3 --version
```

## Virtual environments in Python 2

virtualenv env-py2

source env-py2/bin/activate

(note change in prompt)

*Python 3 has a more elaborate set of tools for managing virtual environments*

## Installing from the Python Package Index (pypi)

See pypi.python.org

```
pip install ofcourse
```
*takes some time to install, note dependency resolution and warnings*

```
## ofcourse: Populating a new course with example content

mkdir ofcourse-demo

cd ofcourse-demo

ofcourse new

ls

ls -lR people
```
*note file and directory structure*

```
ofcourse validate
```

    # ofcourse run
    # point browser at https://localhost:5000

## ofcourse: Pulling in existing course content

```
cd ..

git clone --depth=1 https://github.com/ritjoe/hfoss

cd hfoss

ls

ls -lR people

ofcourse validate

    # ofcourse run
    # point browser at https://localhost:5000

```

