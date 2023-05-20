# Gym_Git_Exerecise-Solutions
```
BUNDLE 1
=======
EXERCISE 1
----------
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~ (main)
$ mkdir Gym-git-exercise

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~ (main)
$ cd Gym-git-exercise

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git init
Initialized empty Git repository in C:/Users/LENOVO/Gym-git-exercise/.git/

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (master)
$ git branch -m main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git commit -m "renamed master branch to 'main'"
On branch main

Initial commit

nothing to commit (create/copy files and use "git add" to track)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git remote add origin https://github.com/gitarecy/Gym_Git_Exerecise-Solutions

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git pull origin main
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 608 bytes | 38.00 KiB/s, done.
From https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git push --set-upstream origin main
Everything up-to-date
branch 'main' set up to track 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ touch file.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git commit -m "Added file"
[main 7c0f44e] Added file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 file.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 273 bytes | 136.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   7732f3a..7c0f44e  main -> main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git checkout -b dev
Switched to a new branch 'dev'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git checkout -b test
Switched to a new branch 'test'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (test)
$ git checkout dev
Switched to branch 'dev'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git branch -D test
Deleted branch test (was 7c0f44e).



EXERCISE 2
----------
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ vi home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git add .
warning: in the working copy of 'home.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash save "Stashing changes for home.html"
Saved working directory and index state On dev: Stashing changes for home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ vi about.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git add .
warning: in the working copy of 'about.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash save "Stashing changes for about.html"
Saved working directory and index state On dev: Stashing changes for about.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ vi team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git add .
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash save "Stashing changes for team.html"
Saved working directory and index state On dev: Stashing changes for team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash list
stash@{0}: On dev: Stashing changes for team.html
stash@{1}: On dev: Stashing changes for about.html
stash@{2}: On dev: Stashing changes for home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (a627c5e6768448b1ee89dcad04ea5912941313c1)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (625ad1fa08e7e1fed5941c935b05d19c72087382)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash list
stash@{0}: On dev: Stashing changes for team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git commit -m "stash pops for both home and about html pages"
[dev 9ea42a8] stash pops for both home and about html pages
 2 files changed, 30 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash list
stash@{0}: On dev: Stashing changes for team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git stash pop stash@{0}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (f16bca122f201b7e0e475162c706f78e80b0a4fa)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git reset --hard HEAD
HEAD is now at 9ea42a8 stash pops for both home and about html pages

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ ls
README.md  about.html  file.txt  home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git commit -m "adding about and home"
On branch dev
nothing to commit, working tree clean

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (dev)
$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 504 bytes | 252.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/gitarecy/Gym_Git_Exerecise-Solutions/pull/new/dev
remote:
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 * [new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.




```
```
BUNDLE 2
-------
EXERCISE 1
---------



```
