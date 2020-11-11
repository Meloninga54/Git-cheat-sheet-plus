# A few things I had to figure out:

## 1. Pulling any changes to a repository that you forked from:

From [this](https://stackoverflow.com/a/7244456/) answer on stackoverflow:

- Add the remote, call it "upstream":

	`git remote add upstream https://github.com/whoever/whatever.git`

- Fetch all the branches of that remote into remote-tracking branches, such as upstream/main or upstream/master:

	`git fetch upstream`

- Make sure that you're on your main branch:

	`git checkout main`

- Rewrite your main branch so that any commits of yours that aren't already in upstream/main are replayed on top of that other branch:

	`git rebase upstream/main`

**Note:** the update is local, after this you'll have to push to the forked repository on github.

## 2. Permanently delete commits from repository:

From [here](https://gist.github.com/dsci/1347672):

- First, check out the commit you wish to go back to (get sha-1[commit ID] from git log)
	`git reset --hard 9d3c3a0caa7f7b35ef15adb96fc80fcbb59ac72a`

- Then do a forced update.
	`git push origin +9d3c3a0caa7f7b35ef15adb96fc80fcbb59ac72a^:develop`

- Push specific commit
	`git push origin 9d3c3a0caa7f7b35ef15adb96fc80fcbb59ac72a:develop`


*Check out a much lazier .txt version of this document [here](git_hacks.txt)*