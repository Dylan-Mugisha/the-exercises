# Git-Exercises
## bundle1
### exercise1


```bash

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
kings-MacBook-Air:the-exercise king$ git init
Initialized empty Git repository in /Users/king/Desktop/projects/git exercises/the-exercise/.git/
kings-MacBook-Air:the-exercise king$ git add .
kings-MacBook-Air:the-exercise king$ git commit -m 'the first chhange'
[master (root-commit) c2155ca] the first chhange
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.md
kings-MacBook-Air:the-exercise king$ git remote add origin https://github.com/Dylan-Mugisha/the-exercises.git
kings-MacBook-Air:the-exercise king$ git push -u origin main
error: src refspec main does not match any.
error: failed to push some refs to 'https://github.com/Dylan-Mugisha/the-exercises.git'
kings-MacBook-Air:the-exercise king$ git push
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

kings-MacBook-Air:the-exercise king$ 
kings-MacBook-Air:the-exercise king$  git push --set-upstream origin master
Counting objects: 3, done.
Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/Dylan-Mugisha/the-exercises.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
kings-MacBook-Air:the-exercise king$ git branch -M main
kings-MacBook-Air:the-exercise king$ git checkout -b dev
Switched to a new branch 'dev'
kings-MacBook-Air:the-exercise king$ git checkout -b text
Switched to a new branch 'text'
kings-MacBook-Air:the-exercise king$ git checkout dev
Switched to branch 'dev'
kings-MacBook-Air:the-exercise king$ git remove test
git: 'remove' is not a git command. See 'git --help'.

The most similar command is
        remote
kings-MacBook-Air:the-exercise king$ git branch -D test
error: branch 'test' not found.
kings-MacBook-Air:the-exercise king$ git branch --delete test
error: branch 'test' not found.
kings-MacBook-Air:the-exercise king$ git branch -D text
Deleted branch text (was c2155ca).
kings-MacBook-Air:the-exercise king$ 
```

### exercises2
```bash

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
kings-MacBook-Air:the-exercise king$ git init
Initialized empty Git repository in /Users/king/Desktop/projects/git exercises/the-exercise/.git/
kings-MacBook-Air:the-exercise king$ git add .
kings-MacBook-Air:the-exercise king$ git commit -m 'the first chhange'
[master (root-commit) c2155ca] the first chhange
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.md
kings-MacBook-Air:the-exercise king$ git remote add origin https://github.com/Dylan-Mugisha/the-exercises.git
kings-MacBook-Air:the-exercise king$ git push -u origin main
kings-MacBook-Air:the-exercise king$ git add home.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git add about.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash list
stash@{0}: WIP on dev: c2155ca the first chhange
stash@{1}: WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git add team.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash list
stash@{0}: WIP on dev: c2155ca the first chhange
stash@{1}: WIP on dev: c2155ca the first chhange
stash@{2}: WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash pop stash@{2}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        about.html
        team.html

Dropped stash@{2} (a7e3b412eab9406001cbda90e53ba4ed693902ac)
kings-MacBook-Air:the-exercise king$ git stash pop stash@{2}
stash@{2} is not a valid reference
kings-MacBook-Air:the-exercise king$ git stash pop stash@{1}
error: The following untracked working tree files would be overwritten by merge:
        about.html
Please move or remove them before you merge.
Aborting
kings-MacBook-Air:the-exercise king$ git stash list
stash@{0}: WIP on dev: c2155ca the first chhange
stash@{1}: WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        team.html

Dropped stash@{1} (24d07d2b467ee7190bee347d819d0a1ed940d627)
kings-MacBook-Air:the-exercise king$ git reset -hard
error: did you mean `--hard` (with two dashes ?)
kings-MacBook-Air:the-exercise king$ git reset --hard
HEAD is now at c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ 
```
## bundle2
### exercises1
```bash

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
kings-MacBook-Air:the-exercise king$ git init
Initialized empty Git repository in /Users/king/Desktop/projects/git exercises/the-exercise/.git/
kings-MacBook-Air:the-exercise king$ git add .
kings-MacBook-Air:the-exercise king$ git commit -m 'the first chhange'
[master (root-commit) c2155ca] the first chhange
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.md
kings-MacBook-Air:the-exercise king$ git remote add origin https://github.com/Dylan-Mugisha/the-exercises.git
kings-MacBook-Air:the-exercise king$ git push -u origin main
kings-MacBook-Air:the-exercise king$ git add home.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git add about.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash list
stash@{0}: WIP on dev: c2155ca the first chhange
stash@{1}: WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git add team.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash list
stash@{0}: WIP on dev: c2155ca the first chhange
stash@{1}: WIP on dev: c2155ca the first chhange
stash@{2}: WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash pop stash@{2}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        about.html
        team.html

Dropped stash@{2} (a7e3b412eab9406001cbda90e53ba4ed693902ac)
kings-MacBook-Air:the-exercise king$ git checkout -b ft/bundle-2
M       readme.md
Switched to a new branch 'ft/bundle-2'
kings-MacBook-Air:the-exercise king$ git add services.html
kings-MacBook-Air:the-exercise king$ git commit -m 'the service page '
[ft/bundle-2 cffa23f] the service page
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 12 insertions(+)
 create mode 100644 services.html
kings-MacBook-Air:the-exercise king$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

kings-MacBook-Air:the-exercise king$ git push --set-upstream origin ft/bundle-2
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 479 bytes | 479.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Dylan-Mugisha/the-exercises/pull/new/ft/bundle-2
remote: 
To https://github.com/Dylan-Mugisha/the-exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
kings-MacBook-Air:the-exercise king$ 
```
### exexrces2
```bash

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
kings-MacBook-Air:the-exercise king$ git init
Initialized empty Git repository in /Users/king/Desktop/projects/git exercises/the-exercise/.git/
kings-MacBook-Air:the-exercise king$ git add .
kings-MacBook-Air:the-exercise king$ git commit -m 'the first chhange'
[master (root-commit) c2155ca] the first chhange
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.md
kings-MacBook-Air:the-exercise king$ git remote add origin https://github.com/Dylan-Mugisha/the-exercises.git
kings-MacBook-Air:the-exercise king$ git push -u origin main
kings-MacBook-Air:the-exercise king$ git add home.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git add about.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash list
stash@{0}: WIP on dev: c2155ca the first chhange
stash@{1}: WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git add team.html
kings-MacBook-Air:the-exercise king$ git stash
Saved working directory and index state WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash list
stash@{0}: WIP on dev: c2155ca the first chhange
stash@{1}: WIP on dev: c2155ca the first chhange
stash@{2}: WIP on dev: c2155ca the first chhange
kings-MacBook-Air:the-exercise king$ git stash pop stash@{2}
On branch dev
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        about.html
        team.html

Dropped stash@{2} (a7e3b412eab9406001cbda90e53ba4ed693902ac)
kings-MacBook-Air:the-exercise king$ git checkout -b ft/bundle-2
M       readme.md
Switched to a new branch 'ft/bundle-2'
kings-MacBook-Air:the-exercise king$ git add services.html
kings-MacBook-Air:the-exercise king$ git commit -m 'the service page '
[ft/bundle-2 cffa23f] the service page
kings-MacBook-Air:the-exercise king$ git checkout main
M       readme.md
Switched to branch 'main'
Your branch is up to date with 'origin/master'.
kings-MacBook-Air:the-exercise king$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), done.
From https://github.com/Dylan-Mugisha/the-exercises
   c2155ca..2678b1d  master     -> origin/master
Updating c2155ca..2678b1d
Fast-forward
 services.html | 12 ++++++++++++
 1 file changed, 12 insertions(+)
 create mode 100644 services.html
kings-MacBook-Air:the-exercise king$ git checkout -b ft/service-redesign
M       readme.md
Switched to a new branch 'ft/service-redesign'
kings-MacBook-Air:the-exercise king$ git commit -m 'some changes added to service page'
On branch ft/service-redesign
Changes not staged for commit:
        modified:   readme.md
        modified:   services.html

Untracked files:
        team.html

no changes added to commit
kings-MacBook-Air:the-exercise king$ git add -asll
error: unknown switch `a'
usage: git add [<options>] [--] <pathspec>...

    -n, --dry-run         dry run
    -v, --verbose         be verbose

    -i, --interactive     interactive picking
    -p, --patch           select hunks interactively
    -e, --edit            edit current diff and apply
    -f, --force           allow adding otherwise ignored files
    -u, --update          update tracked files
    -N, --intent-to-add   record only the fact that the path will be added later
    -A, --all             add changes from all tracked and untracked files
    --ignore-removal      ignore paths removed in the working tree (same as --no-all)
    --refresh             don't add, only refresh the index
    --ignore-errors       just skip files which cannot be added because of errors
    --ignore-missing      check if - even missing - files are ignored in dry run
    --chmod <(+/-)x>      override the executable bit of the listed files

kings-MacBook-Air:the-exercise king$ git add -all
error: did you mean `--all` (with two dashes ?)
kings-MacBook-Air:the-exercise king$ git add --all
kings-MacBook-Air:the-exercise king$ git commit -m 'some changes added to service page'
[ft/service-redesign 3153baf] some changes added to service page
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 3 files changed, 289 insertions(+)
 create mode 100644 team.html
kings-MacBook-Air:the-exercise king$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

kings-MacBook-Air:the-exercise king$ git push --set-upstream origin ft/service-redesign
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 2.28 KiB | 2.28 MiB/s, done.
Total 5 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Dylan-Mugisha/the-exercises/pull/new/ft/service-redesign
remote: 
To https://github.com/Dylan-Mugisha/the-exercises.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
Branch 'ft/service-redesign' set up to track remote branch 'ft/service-redesign' from 'origin'.
kings-MacBook-Air:the-exercise king$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/master'.
kings-MacBook-Air:the-exercise king$ git merge ft/service-redesign
Updating 2678b1d..3153baf
Fast-forward
 readme.md     | 276 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 services.html |   1 +
 team.html     |  12 +++++++
 3 files changed, 289 insertions(+)
 create mode 100644 team.html
kings-MacBook-Air:the-exercise king$ git push
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:master

To push to the branch of the same name on the remote, use

    git push origin main

kings-MacBook-Air:the-exercise king$  git push origin main
Total 0 (delta 0), reused 0 (delta 0)
remote: 
remote: Create a pull request for 'main' on GitHub by visiting:
remote:      https://github.com/Dylan-Mugisha/the-exercises/pull/new/main
remote: 
To https://github.com/Dylan-Mugisha/the-exercises.git
 * [new branch]      main -> main
kings-MacBook-Air:the-exercise king$ git checkout main
Already on 'main'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
kings-MacBook-Air:the-exercise king$ git commit -m 'change again in service'
On branch main
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
        modified:   services.html

no changes added to commit
kings-MacBook-Air:the-exercise king$ git add --add
error: unknown option `add'
usage: git add [<options>] [--] <pathspec>...

    -n, --dry-run         dry run
    -v, --verbose         be verbose

    -i, --interactive     interactive picking
    -p, --patch           select hunks interactively
    -e, --edit            edit current diff and apply
    -f, --force           allow adding otherwise ignored files
    -u, --update          update tracked files
    -N, --intent-to-add   record only the fact that the path will be added later
    -A, --all             add changes from all tracked and untracked files
    --ignore-removal      ignore paths removed in the working tree (same as --no-all)
    --refresh             don't add, only refresh the index
    --ignore-errors       just skip files which cannot be added because of errors
    --ignore-missing      check if - even missing - files are ignored in dry run
    --chmod <(+/-)x>      override the executable bit of the listed files

kings-MacBook-Air:the-exercise king$ git add services.html
kings-MacBook-Air:the-exercise king$ git commit -m 'the change'
[main 77a88a6] the change
 Committer: king <king@kings-MacBook-Air.local>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly. Run the
following command and follow the instructions in your editor to edit
your configuration file:

    git config --global --edit

After doing this, you may fix the identity used for this commit with:

    git commit --amend --reset-author

 1 file changed, 3 insertions(+), 2 deletions(-)
kings-MacBook-Air:the-exercise king$ git push
fatal: The upstream branch of your current branch does not match
the name of your current branch.  To push to the upstream branch
on the remote, use

    git push origin HEAD:master

To push to the branch of the same name on the remote, use

    git push origin main

kings-MacBook-Air:the-exercise king$ git push origin main
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 397 bytes | 397.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Dylan-Mugisha/the-exercises.git
   3153baf..77a88a6  main -> main
kings-MacBook-Air:the-exercise king$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
kings-MacBook-Air:the-exercise king$ git diff head
kings-MacBook-Air:the-exercise king$ git diff HEAD
kings-MacBook-Air:the-exercise king$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)
kings-MacBook-Air:the-exercise king$ git merge ft/service-redesign
Already up to date.
kings-MacBook-Air:the-exercise king$ 
```