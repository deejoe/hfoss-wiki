
# Git format-patch short demo

## Set up first repo

### Create a directory structure to contain any mess

```
 mkdir format-patch-demo
 cd format-patch-demo
 mkdir upstream
 cd upstream
```

### Create an initial file

```
 echo red > colors.txt
 echo green >> colors.txt
 echo blue >> colors.txt
```

### Add and commit it

```
 git init
 git add colors.txt 
 git commit -m "Add RGB version, initial commit"
```

## Make changes in a second repo

### Clone and change to clone

```
 cd ..
 git clone upstream downstream
 cd downstream
```


### Create a series of commits

```
 sed -i.bak -e 's/red/red\norange/' colors.txt 
 ls -al
 git add colors.txt
 git commit -m "Add orange"
```
```
 sed -i.bak -e 's/orange/orange\nyellow/' colors.txt 
 git add colors.txt
 git commit -m "Add yellow"
```

```
 sed -i.bak -e 's/blue/blue\nindigo/' colors.txt 
 sed -i.bak -e 's/indigo/indigo\nviolet/' colors.txt 
```
### Inspect the changes, add, and commit them

```
 cat colors.txt
```

```
 git add colors.txt
 git commit -m "Add indigo and violet"
```

### All in master like a demo cowboy oh well

```
 git status
 git log
```

## Create and inspect the patches

```
 git format-patch HEAD~3 HEAD
```

```
 ls
 less *.patch
```

**NB**: One may wish to add *.patch to either .git/info/excludes or to .gitignore
