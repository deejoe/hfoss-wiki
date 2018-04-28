
A software `master` branch *by convention* always holds production quality
code, well tested, containing no known bugs, etc.

For our course, **production ready** means including all assignment
key-value pairs the student has submitted upstream to date. It should be
the **best**, most complete version of the student's YAML file.

Maintain your fork of the `hfoss` class repository to keep it up-to-date
both with

  * the upstream class repository
  * the changes you make in feature branches

Do the former by frequently pulling, or fetching then merging, from the
upstream class repository.

The latter is more tricky.  In order to practice using feature branches,
create a branch for each assignment you submit.  Then add a new YAML key and
its corresponding URL value while in that branch.  Then submit a PR from
that branch.

Doing so repeatedly goes smoothly so long as each addition is submitted,
merged upstream, and the upstream branch incorporated into the local working
master before creating the next feature branch.  In other words, all tends
to go well so long as each change propogates across all the relevant
branches before another change is introduced.

Here, we see that commit C makes it all the way upstream and all the way
back into the student fork before D is introduced.  Because C is already
included when D comes into each branch, no merge conflict arises:


```
upstream/hfoss/master:          A---B-------C-------D--
                                 \   \     / \     / \
student/hfoss/feature[1,2...]     \   \   C   \   D   \
                                   \   \ /     \ /     \
student/hfoss/master:               A---B-------C-------D
```


But, should one introduce different changes into parallel branches, that is,
submitting a second or subsequent assignment (D below) before a previous
assignment (C below) is merged upstream and pulled back in, a merge conflict
(X) can occur:

```
upstream/hfoss/master:  A---B-------C---X-
                         \         /   / 
                      	  \       C   / student/hfoss/feature1
                           \     /   /   
student/hfoss/master:       A---B --/-----
                                 \ /
                                  D     student/hfoss/feature2
```

In a simple and common case, each commit adds a line to the end of the file. 
A merge conflict arises because the merge algorithm cannot resolve the
order in which to place the two new lines: Which line should be at the end?

While this simple misordering can be fairly straightforward to resolve, more
complicated conflicts can arise.

Avoid these conflicts by ensuring each of your feature branches
can be merged into your own `master` branch

```
upstream/hfoss/master:          A---B-------C---D--
                                 \   \     /   /
student/hfoss/feature[1,2...]     \   \   C   D  
                                   \   \ / \ / \
student/hfoss/master:               A---B---C---D--
```

Again, changes from C are already included by the time the changes for D are
introduced, precluding a conflict from C and D. 

