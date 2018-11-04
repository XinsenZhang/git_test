# git_test

* <<<<<<< HEAD
* Creating a new branck is quick & simple.
* =======
* Creating a new branck is quick AND simple.
* >>>>>>> feature1
* using git log --graph can see the combination graph of branches
* do some recap and test
	* clone can just get the file, not the log
	* push just push the file, including all the branches, master etc
	* using git checkout -- filename can recover the file from stage
	* now what you should do is to get how to recover from git repository
		* with the command
			* git reset HEAD filename 

* git checkout -b branchname 
	* the same as:
		1. git branch branchname
			* create a branch
		2. git checkout branchname
			* switch to the branch
* branch is just like parallel universe
	* work on a branch does not matter on work via master
	* master is the most stable timeline
	* dev is a temporary copy timeline, which is a branch
	* colleagues A and B work on two different branches  from master and dev
		* sometimes merged into dev( but I think most time)
		* seldomly work on master
* during merge
	* git merge branchname
		* merge the specific branch into the current HEAD towards branch
		* Fast Forword Mode
		* drawbacks:
			* no log information
				* no historical log
	* git merge --no-ff -m "messsage content" branch name
		* disable Fast Forword Mode
		* Enable "Recursive" strategy
		* point:
			* maintain the log on the merging branch
			* simutanously commit, which implies the parameter -m

* What if you are working on branch dev, but you are assigned to work on a bug, named  issure-101
	* store the spot where your work lies on, using the command 
		* git stash
	* using git stash list to get the list of stash
	* two method to restore the content storage in stash
		* using git stash apply
			* after then, using git stash drop to delete the stashed spot in the stash list
		* another method is to use
			* git stash pop
				* restore the spot
				* semontaneously delete the spot in the list
* A branch without merged will raise an error if you want delete it via parameter -d
	*solution:
		* using parameter -D to forcely delete it
		* git branch -D branchname
