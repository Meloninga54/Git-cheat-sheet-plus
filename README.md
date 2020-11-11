# A few things I had to figure out:

## Pulling any changes to a repository that you forked from:

From [this](https://stackoverflow.com/a/7244456/) answer on stackoverflow:

- Add the remote, call it "upstream":

>git remote add upstream https://github.com/whoever/whatever.git

- Fetch all the branches of that remote into remote-tracking branches,
- such as upstream/main or upstream/master:

>git fetch upstream

- Make sure that you're on your main branch:

>git checkout main

- Rewrite your main branch so that any commits of yours that
- aren't already in upstream/main are replayed on top of that
- other branch:

>git rebase upstream/main

**Note:** the update is local, after this you'll have to push to the forked repository on github.

