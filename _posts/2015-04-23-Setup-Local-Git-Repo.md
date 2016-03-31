---
layout: post
title:  Setup Local Git Repo
---


If you are working on some confidential project, it is not a good idea to use github to do the version control and backup. A local repository may be necessary for such purpose.

For example, repository will be created locally under USB disk /media/usb/repo
Working directory is under /home/jun/code

	$ cd /media/usb/repo
	$ git init --bare safe.git
	$ cd /home/jun
	$ git clone /media/usb/repo/safe.git code

Then we do a test to see whether it works.

	$ cd /home/jun/code
	$ echo "This is a test file" > test.txt
	$ git add test.txt
	$ git commit -m "What a wonderful world to commit!"
	$ git push

It's done~~ 


Additional providing some useful git commands. 

	$ git init
	$ git init --bare myproject.git
	
	$ git config -l
	$ git config --global user.name "yourname"
	$ git config --global user.email "yourname@somewhere"
	$ git config --global core.editor vim
	$ git config --global merge.tool vimdiff
	$ git config --global push.default simple
	
	$ git add .
	$ git commit -m "First commit"
	$ git commit --amend
	$ git push
	$ git pull
	$ git checkout FILENAME
	$ git checkout BRANCHNAME
	$ git branch BRANCHNAME
	$ git rm --cached FILENAME
	$ git stash
	$ git stash pop
	# git reset HEAD




For more information, refer to

[Git Documentation](http://git-scm.com/doc)

[CSDN blog of ithomer (Chinese)](http://blog.csdn.net/ithomer/article/details/7529022)

	$ git checkout -b fixes 1b6d