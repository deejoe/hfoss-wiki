
You should maintain your fork of the `hfoss` class repository to keep it
up-to-date both with

  * the upstream class repository
  * the changes you've made in feature branches

You can do the former by frequently pulling or fetching then merging from
the upstream class repository.

The latter is more tricky. In order to give you practice using feature
branches, we ask that you create a branch for each assignment you submit.
You then add the a new YAML key and a corresponding URL value in that
branch, and then submit a PR from that branch.

This alone is fine so long as your feature branches are submitted with
sufficient time for them to be merged into the upstream class repository,
and then incorporated into the master branch of your fork, and from which
you then 



upstream/hfoss/master:          A---B-------C---D-------E--
                                 \   \     /     \     /
student/hfoss/feature[1,2...]     \   \   C       \   E  
                                   \   \ /         \ /  
student/hfoss/master:               A---B-----------D---E--


But in the case where a student tries to submit two assignments in parallel,
(here shown as D and E) this can generate a merge conflict:



upstream/hfoss/master:  A---B-------C---X
                         \         /   / 
                      	  \       C   / student/hfoss/feature1
                           \     /   /   
student/hfoss/master:       A---B   /
                                 \ /
                                  D     student/hfoss/feature2

In the simplest case, each commit represents adding a line to the end of the
file, and the merge conflict arises from the merge algorithm not knowing in
which order to place the two new lines. So, the merge conflict can be
fairly straightforward to resolve.

But, if the student's master branch does not merge commits from upstream for
a long time, even more, and more difficult-to-resolve, conflicts can arise.

A way to avoid this is to make sure 

upstream/hfoss/master:          A---B-------C---D-------F--
                                 \   \     /     \     /
student/hfoss/feature[1,2...]     \   \   C       \   F  
                                   \   \ / \       \ / \
student/hfoss/master:               A---B---C-------D---F--
