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
$ git rm PROJECTS.md
