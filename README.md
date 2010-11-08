# Title
 
## Description

### DONE 

### TODO

v 0.1.2

---

[ling](http://www.google.com)


Typical-Git-workflow

git clone git://github.com/bard/sameplace.git
git branch fix_for_foobar
git checkout fix_for_foobar
git commit -a -m 'Join Room Dialog: foobar functionality was broken.  Fixed.'

git checkout master
git pull

git rebase fix_for_foobar

git format-patch origin

[https://github.com/bard/sameplace/wiki/Typical-Git-workflow]

+++++++++++++++++++++++++
Multi-staged deployment with versioning using git.

   1. Create Version for each sprint
   2. Deploy Version after each Demo
   3. Create bug fixes on Version Branch
   4. Deploy Version branch and tag it with a release number (repeat as necessary)
   5. Merge down bug fixes to master


For each new version, create a remote branch that represents a version.
	git push origin origin:refs/heads/version-0.1
Git does not allow you to work in remote branches, so create a local git branch that tracks your remote branch (version).
	git branch --track v0.1 origin/version-0.1
Checkout your version branch, fix bug, and do a git push. 
Prior to each deployment, create a git remote tag incremented for the next release.

git tag release-0.1.1
git push --tags

Repeat tagging procedure for each bug until next version.
After your are finished with a particular Version, merge changes back to master.

git checkout master
git merge version-0.1
	
[http://blog.elctech.com/2008/12/17/multi-staged-deployment-with-versioning-using-git/]

What do maintainers do?

git checkout upstream
git pull origin
git checkout topic/a
git merge upstream
git checkout topic/b
git merge upstream
git checkout master
git merge topic/a  topic/b
# do the release thing
git commit

[http://www.golden-gryphon.com/software/misc/packaging.html]

High-level Best Practices in Software Configuration Management
[http://www.perforce.com/perforce/papers/bestpractices.html]
