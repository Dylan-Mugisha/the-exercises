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