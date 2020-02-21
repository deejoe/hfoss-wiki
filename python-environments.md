
# Python virtual environments and pip

## Python versions

```
which python

which python3

python --version

python3 --version
```

## Virtual environments in Python 2 (deprecated)

```
virtualenv env-py2

source env-py2/bin/activate
```

(note change in prompt)

## Virtual environments in Python 3 

```
virtualenv -p python3 env-py3

source env-py3/bin/activate
```

*For Python 3 one might also use* `pipenv`

## Installing from the Python Package Index (pypi)

See pypi.python.org

```
pip install ofcourse
```

*takes some time to install, note dependency resolution and warnings*


## ofcourse: Populating a new course with example content

```
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
```

    # ofcourse run
    # point browser at https://localhost:5000



