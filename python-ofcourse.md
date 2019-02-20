
# Installing ofcourse in a Python virtual environment

## Installing from the Python Package Index (pypi)

See [https://docs.python.org/3/tutorial/venv.html](pypi.python.org)

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

```
 ofcourse run
```

point browser at [https://localhost:5000]([https://localhost:5000)


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

