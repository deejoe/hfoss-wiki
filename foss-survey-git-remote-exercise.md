
Using gitbash, PuTTY or similar, ssh into ```saskia.igm.rit.edu``` or open 
git bash.

Clone `https://kgcoe-git.rit.edu/djaigm/hfoss-2195`

Change into `hfoss-2195`

Make a new directory called `scratch-YOURID` (eg, `djaigm`, `xyz5432`)

Using an editor on saskia, or some other means (eg, creating the file on
another host and transferring it to saskia via ```filezilla```), create a
file in the directory with the same basename as your yaml file, but with the
filename extension ```.txt``` (eg, mine might be ```deejoe.txt```)

Into this file place a partial list of FOSS programs found on the classroom
computers.

You may wish to add this work to a feature branch, also matching the
basename of your ```.yaml``` file, eg

```git checkout -b <deejoe>```

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

Monitor the state of this repo. 

Once some of your classmates have pushed their own files to the upstream
repo, fetch those branches and use the information within them to expand
your list of software packages. You can try to merge their branches into
yours as a good exercise on how to resolve merge conflicts.

Edit, add, commit, and push again.  We will aim eventually to have a more
full list of packages to merge into the ```master``` branch.

