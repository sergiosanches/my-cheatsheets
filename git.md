## git
_learning by cheatsheet_


#### check the log
```bash
git log --oneline			# show one commit per line
git log -<limit>			# limit number of commits shown
git log -p					# display full diff for each commit
git log --graph --oneline --decorate --date-order --color	# pretty graphed log history
```


#### check differences
```bash
git diff HEAD				# show difference between working directory and last commit
git diff HEAD^(^^...)		# compare the version before (^) the last commit and the last commit, each '^' symbol means one more version backwards
```


#### check branches
```bash
git remote show origin		# show info about all branches on origin, and about local branches configuration for push/pull
git branch -vv				# show local branches, sha1, ref, latest commit msg
```


#### rebase
```bash
git rebase <base>			# rebase the current branch onto <base>
# in case of conflicts:
  fix conflicts manually	# text editor to the rescue
  git add <fixed files>		# add the resolution back on track
  git rebase --continue		# proceed
```


#### stash
```bash
git stash show -p stash@{0}	# diff against stashed entry
```


#### update
```bash
git remote update -p		# fetch updates for the remotes and prune stale branches
git merge --ff-only @{u}	# update the local branch
```
