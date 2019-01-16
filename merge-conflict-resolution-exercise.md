
# HFOSS Exercise: Merge conflicts

## Merge conflict creation and resolution

The following is an annotated version of a script that demonstrates the
creation and resolution of a merge commit.

It is followed by the more compact, more succinct version with blank lines
and comments removed.

The statements in which `echo` is used to redirect STDOUT text to `file.txt`
are a quick and dirty way to script what more likely would be done through
an interactive session with a text editor.  

If you work through the example by typing it in (which is probably the best
way to get the most out of this example) then you may wish to invoke your
editor on the target file in place of all `echo` statements but the first
one.

### Commented version

```

# set up the directory

## clean up any previous one
ls conflict-resolution
echo OK to delete conflict-resolution? If no, hit Ctrl-C, if yes hit any other key
read
rm -rf conflict-resolution

## make a new one
mkdir conflict-resolution
cd conflict-resolution

# create the file

ls
cat file.txt

echo firstline > file.txt

ls
cat file.txt

# initialize repo and make first commit

git init
git status

git add file.txt
git commit -m "first commit is a file with a single line"
git tag firstcommit

git status
git log
git ls-tree master .

# UPPERNEXT
## this sets up one side of the conflict

git checkout -b uppernext
git status

echo NEXTLINE >> file.txt
cat file.txt
git status

git add file.txt
git commit -m "commit with next line in UPPERCASE"
git tag uppercommit

git status
git log
cat file.txt

# get back on master branch

git checkout master
cat file.txt
git status
git log


# lowernext
## this sets up the other side of the conflict

git checkout -b lowernext
git status

echo nextline >> file.txt
cat file.txt
git status

git add file.txt
git commit -m "commit with next line in lowercase"
git tag lowercommit

git status
git log
cat file.txt

# get back on master branch

git checkout master
cat file.txt
git status
git log

# merge one

git merge uppernext
git status

git merge lowernext
git status

cat file.txt

echo firstline > file.txt
echo nextline >> file.txt

cat file.txt
git status

git add file.txt
git status
git commit -m "resolve the conflict by creating, adding, and commiting a new file. Usually one would edit the file."
git status
git log --graph --pretty=oneline

git diff uppercommit lowercommit

cd ..

```

### Compact version


```
echo OK to delete conflict-resolution? If no, hit Ctrl-C, if yes hit any other key
read
rm -rf conflict-resolution
mkdir conflict-resolution
cd conflict-resolution
echo firstline > file.txt
git init
git add file.txt
git commit -m "first commit is a file with a single line"
git tag firstcommit
git ls-tree master .
git checkout -b uppernext
echo NEXTLINE >> file.txt
git add file.txt
git commit -m "commit with next line in UPPERCASE"
git tag uppercommit
git checkout master
git checkout -b lowernext
echo nextline >> file.txt
git add file.txt
git commit -m "commit with next line in lowercase"
git tag lowercommit
git checkout master
git merge uppernext
git merge lowernext
echo firstline > file.txt
echo nextline >> file.txt
git add file.txt
git commit -m "resolve the conflict by creating, adding, and commiting a new file. Usually one would edit the file."
git diff uppercommit lowercommit
cd ..
```