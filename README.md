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

14. Undoing Things
$ git commit --amend

15. Unstaging a Staged File
git reset HEAD fileToUnstage.md

