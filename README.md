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
