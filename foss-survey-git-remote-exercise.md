

Using gitbash, PuTTY or similar, ssh into ```saskia.igm.rit.edu```

Change into the ```hfoss18s``` directory you created earlier.

Make a new directory called ```hfoss-scratch```

Change into this directory.

Initialize an empty git repo with ```git init```

Using an editor on saskia, or some other means (eg, creating the file on
another host and transferring it to saskia via ```filezilla```), create a
file in the directory with the same basename as your yaml file, but with the
filename extension ```.txt``` (eg, mine might be ```deejoe.txt```)

Into this file place a partial list of FOSS programs found on the classroom
computers.

Add the file to your git repo, and then commit it to the git repo.  Follow
your progress using ```git status``` and ```git log``` as you go.

Add my djaigm/hfoss-scratch repo on the KGCOE GitLab server as a remote for
your repo.  

```git remote add upstream https://kgcoe-git.rit.edu/djaigm/hfoss-scratch```


Fetch, and then push to your own branch on the repo, eg:

```git push upstream \<deejoe>```

(using your own nickname in place of \<deejoe>)

Monitor the state of this repo. 

Once some of your classmates have pushed their own files to the upstream
repo, fetch those branches and use the information within them to expand
your list of software packages.

Edit, add, commit, and push again.  We will aim eventually to have a more
full list of packages to merge into the ```master``` branch.

