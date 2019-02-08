
Using gitbash, PuTTY or similar, ssh into ```saskia.igm.rit.edu```

Make a new directory ```hfoss19s``` and change into it:

```
mkdir hfoss19s
cd hfoss19s
```

Make a new directory called ```hfoss-scratch```

Change into this directory.

Initialize an empty git repo with ```git init```

Take a look through the software installed on the lab machine you are using, keeping an eye out for software you recognize as being FOSS. If in doubt, launch the software and look in its *help* or *about* interface, or do a web search for it.

Using an editor on saskia, or some other means (eg, creating the file on
another host and transferring it to saskia via ```filezilla```), create a
text file in your ```hfoss19s/hfoss-scratch``` directory.  It should have the same basename as your yaml file, but with the filename extension ```.txt``` (eg, mine might be ```deejoe.txt```)

Into this file place a partial list of FOSS programs found on the classroom
computers.

You may wish to add this work to a feature branch, also matching the
basename of your ```.yaml``` file, eg

```git checkout -b ```*deejoe*

Add the file to your git repo, and then commit it to the git repo.  Follow
your progress using ```git status``` and ```git log``` as you go.

Add my djaigm/hfoss-scratch repo on the KGCOE GitLab server as a remote for
your repo.  

```git remote add upstream https://kgcoe-git.rit.edu/djaigm/hfoss-scratch```


Fetch, and then push to your own branch on the repo. 

If you already have your commits in a local branch named after yourself, you
can just

```git push upstream <deejoe>```

If your local working copy has your commits to the default ```master```
branch, you'll need to push it to a different branch on the remote side. 
Give the branch the same name as the name of your yaml file:

```git push upstream master:<deejoe>```

(in either case, using your own nickname in place of <deejoe>)

(If you do not specify the branch to push, you will be prompted to set a default branch to use with this remote.)

Monitor the state of this repo. 

Once some of your classmates have pushed their own files to the upstream
repo, fetch those branches and use the information within them to expand
your list of software packages. You can try to merge their branches into
yours as a good exercise on how to resolve merge conflicts.

Edit, add, commit, and push again.  If we work further with these files, we will aim to have a more
full list of packages to merge into the ```master``` branch.

