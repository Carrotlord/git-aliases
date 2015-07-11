# git-aliases
Some convenience commands for git. The behavior of each alias is described below.

__`git glog2`__ - graphical tree log showing branches and commits in an ascii-art diagram. This is a modified version of [git glog](https://coderwall.com/p/syqplg/glog-a-git-log-alias-for-a-decent-view-of-your-repo) and similar aliases.

__`git ln`__ - _(pronounced "git natural log")_ - Similar to built-in `git log`, but shows recent commits on a single line, with time-ago info and short commit id. Example output:
```
$ git ln
22 minutes ago  | 105f9ed optimize code by YourUserName @ Sat May 16 22:35:01 2015
14 hours ago    | 901c780 refactor by Bob @ Sat May 16 08:35:22 2015
17 hours ago    | 15a3bee security fix by Alice @ Sat May 16 05:35:18 2015
18 hours ago    | 3da1592 security patch by Eve @ Sat May 16 04:35:40 2015
2 days ago      | 160aca5 rebase everything by Mallory @ Thu May 14 12:52:39 2015
5 days ago      | f1b2482 add ui by YourUserName @ Mon May 11 10:17:28 2015
...
```

__`git ln --max-count=n`__ - Same as `git ln`, but shows exactly `n` commits.

__`git whatis <branch or head pointer>`__ - Shows you the commit id of a branch or head pointer. Use `git whatis HEAD` to display the commit id of where you are right now. Use `git whatis master` to display the commit id of the master branch.
```
$ git whatis HEAD
105f9edcd051672459c1038d496a35ccdfc10965
$ git whatis FETCH_HEAD
27f911682d057bc237ecc4c900832552dff07467
$ git whatis master
105f9edcd051672459c1038d496a35ccdfc10965
$ git whatis new-branch-1
61e4523c00bd2233a6a2923669c6823a7cf7c5b6
```

__`git last`__ - Similar to `git ln`, but shows only the most recent commit.

__`git branch-remembers`__ - Lists all branches that "remember" the current commit, HEAD. Doesn't take arguments.

__`git remote-remembers`__ - Lists all remote branches that "remember" the current commit, HEAD. Doesn't take arguments.

__`git mirage <filename>`__ - If you've already commited a file and no longer want to track changes to it, use `git mirage <some file>` to exclude it from future commits.

__`git reveal <filename>`__ - Reveals a file that was hidden by `git mirage`.

__`git stat`__ - Same as built-in `git status`, but is 2 characters shorter.

