# gitDemo

1. Initializing a Repository in an Existing Directory
$ git init

2. Add all existing files
git add *

3. Commit
$ git commit -m 'initial project version'

4. Cloning an Existing Repository
$ git clone https://github.com/libgit2/libgit2
$ git clone https://github.com/libgit2/libgit2 mylibgit

5. Checking the Status of Your Files
$ git status

6. Staging Modified Files
$ git add CONTRIBUTING.md
$ git status

7. Short Status
$ git status -s

8. To see what was changed but not yet staged
$ git diff

9. To see what was staged that will go into next commit
$ git diff --staged

10. Skipping the Staging Area
$ git commit -a -m 'added new benchmarks'

11. Removing Files
$ git rm PROJECTS.md       (also removes the file from your working directory)
$ git rm --cached README   (keep the file in your working tree but remove it from your staging area)
$ git rm log/\*.log        (remove all files with .log extension)

12. Moving/Renaming Files
$ git mv file_from file_to
$ git mv README.md README

13. Viewing the Commit History
$ git log
$ git log -p -2
$ git log --stat
$ git log --pretty=oneline
$ git log --pretty=format:"%h - %an, %ar : %s"
$ git log --pretty=format:"%h %s" --graph
$ git log --since=2.weeks
$ git log --oneline --decorate
$ git log --oneline --decorate --graph --all

Common options to git log:
-p               Show the patch introduced with each commit.
--stat           Show statistics for files modified in each commit.
--shortstat      Display only the changed/insertions/deletions line from the --stat command.
--name-only      Show the list of files modified after the commit information.
--name-status    Show the list of files affected with added/modified/deleted information as well.
--abbrev-commit  Show only the first few characters of the SHA-1 checksum instead of all 40.
--relative-date  Display the date in a relative format (for example, "2 weeksago") instead of using the full date format.
--graph          Display an ASCII graph of the branch and merge history beside the log output.
--pretty         Show commits in an alternate format. Options include oneline, short, full, fuller, and format (where you specify your own format).

Useful options for git log --pretty=format
%H    Commit hash
%h    Abbreviated commit hash
%T    Tree hash
%t    Abbreviated tree hash
%P    Parent hashes
%p    Abbreviated parent hashes
%an   Author name
%ae   Author email
%ad   Author date (format respects the --date=option)
%ar   Author date, relative
%cn   Committer name
%ce   Committer email
%cd   Committer date
%cr   Committer date, relative
%s    Subject

To navigate while in log or diff mode:

Next line:        j / return
Previous line:    k
Next page:        f / space bar
Previous page:    b / w
Quit viewing:     q
Help:             h


14. Undoing Things
$ git commit --amend

15. Unstaging a Staged File
git reset HEAD fileToUnstage.md

16. Unmodifying a Modified File
$ git checkout -- CONTRIBUTING.md

Any changes you made to that file are gone – Git just copied another file over it.

17. Showing Your Remotes
$ git remote
$ git remote -v (shows you the URLs that Git has stored for the )shortname)

18. Adding Remote Repositories
To add a new remote Git repository as a shortname you can reference:
$ git remote add <shortname> <url>

Then you can use the string <shortname> on the command line in lieu of the whole URL.
$ git fetch <shortname>

19. Fetching and Pulling from Your Remotes
$ git fetch [remote-name]
$ git fetch origin

It’s important to note that the git fetch command only downloads the data to your local repository – it doesn’t automatically merge it with any of your work or modify what you’re currently working on. You have to merge it manually into your work when you’re ready.

$ git pull 
Generally fetches data from the server you originally cloned from and automatically tries to merge it into the code you’re currently working on.

20. Pushing to Your Remotes
$ git push [remote-name] [branch-name]
$ git push origin master

21. Inspecting a Remote
$ git remote show origin
$ git remote

22. Removing and Renaming Remotes
$ git remote rename pb paul
$ git remote rm paul

23. Tagging
$ git tag (Listing the available tags in Git)
$ git tag -l "v1.8.5*" (search for tags with a particular pattern)

$ git tag -a v1.4 -m "my version 1.4" (Creating an annotated tag)

$ git tag v1.4-lw (Creating a lightweight tag)

24. Checking out Tags
To put a version of your repository in your working directory that looks like a specific tag, you can create a new branch at a specific tag
$ git checkout -b [branchname] [tagname]
$ git checkout -b version2 v2.0.0
Switched to a new branch 'version2'

25. Creating a New Branch
$ git branch develop

26. Switching Branches
$ git checkout develop
$ git checkout -b hotfix (create a branch and switch to it at the same time)
Switched to a new branch 'hotfix'

27. Merging Branches
$ git checkout master (first, switch to desired branch)
$ git merge hotfix

28. Deleting Branches
$ git branch -d hotfix
Deleted branch hotfix (3a0874c).

29. Basic Merge Conflicts - p.96
$ git mergetool

30. Branch Management
$ git branch (shows a listing of your current branches)
$ git branch -v (shows the last commit on each branch)

$ git branch --merged (shows which branches are already merged into the branch you're on)
$ git branch --no-merged (To see all the branches that contain work you haven't yet merged in)

31. Remote Branches
$ git ls-remote [remote]
$ git remote show [remote]

$ git fetch origin (This command looks up which server “origin” is, fetches any data from it that you don't yet have, and updates your local database, moving your origin/master pointer to its new, more up-to-date position.

32. Pushing
$ git push <remote> <branch>
$ git push origin serverfix