
Create a github account, or identify an existing account to use.

Navigate to the course repository

https://github.com/ritjoe/hfoss

Click the "Fork" button in the upper right.

Switch to a Git Bash or to your favorite git client, and do the following 
(or their equivalents in your client-of-choice):

Clone your fork:

```
git clone https://github.com/myusername/hfoss

cd hfoss
cd ofcourse-content
cd people
```

Check whether the next two levels of subdirectories exist:

```
ls 2020/spring
```

if that gives an error and depending on when you forked, you may need to create these subdirectories:

```
mkdir -p 2020/spring
```

If they exist, descend into them:

```
cd 2020
cd spring
```

Ensure the your position in the filesystem includes the path components `hfoss/ofcourse-content/people/spring/2020`



Create a feature branch:

```
git checkout -b firstflight
```

Open an editor to begin creating your YAML file:

```
vim myusername.yaml
```

Enter the information for the following items:

```
name: 
avatar: 
blog: 
feed: 
email:
major: 
irc: 
rit_dce: 
forges:
  - 
bio: 
hw:
  firstflight:
```

Save your file from the editor.

Add your file to the git index, commit it to your local repo, and push to 
your fork:

```
git add myusername.yaml
git commit -m "Adding YAML file for HFOSS Spring 2019 student myusername"
git push
```

Return to a web browser and navigate to the page for your fork.

Navigate under `branches` to `firstflight`

Click to create a pull request.

