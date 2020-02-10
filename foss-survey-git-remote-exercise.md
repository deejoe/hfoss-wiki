
## Prepare a repository and working directory for your survey results

Using gitbash, PuTTY or similar, ssh into ```saskia.igm.rit.edu``` or open 
git bash.

Clone `https://kgcoe-git.rit.edu/djaigm/hfoss-2195`

Change into `hfoss-2195`

Make a new directory called `survey-YOURID` (eg, `djaigm`, `xyz5432`)

You will place in this directory a file containing a list of (at least some 
of) the free and open source software packages you find installed on the lab 
computers.

Look through the software on the systems. Identify what FOSS you can.

Using an editor on saskia, or some other means (eg, creating the file on
another host and transferring it to saskia via ```filezilla```), create a
file in the directory with the same basename as your yaml file, but with the
filename extension ```.md``` (eg, mine might be ```deejoe.md```)

Into this file place the names, one per line, of the FOSS you found on the 
computer.

You may wish to add this work to a feature branch, also matching the
basename of your ```.yaml``` file, eg

```git checkout -b <deejoe>```

Add the file to your git repo, and then commit it to the git repo.  Follow
your progress using ```git status``` and ```git log``` as you go.

If you already have your commits in a local branch named after yourself, and 
you are on that branch, you can just

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
yours as a good exercise on how to resolve merge conflicts, or you can 
rebase your changes onto theirs.

Edit, add, commit, and push again.  We will aim eventually to have a more
full list of packages to merge into the ```master``` branch.

