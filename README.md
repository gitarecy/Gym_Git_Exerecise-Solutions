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
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (ft/bundle-2)
$ ls
README.md

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (ft/bundle-2)
$ vi services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (ft/bundle-2)
$ ls
README.md  services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (ft/bundle-2)
$ git add .
warning: in the working copy of 'services.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (ft/bundle-2)
$ git commit -m "Added service.html to the ft/bundle-2 branch and made changes"
[ft/bundle-2 142f508] Added service.html to the ft/bundle-2 branch and made changes
 1 file changed, 14 insertions(+)
 create mode 100644 services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 375 bytes | 187.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/gitarecy/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/gitarecy/Gym-Git-Exercise-Solutions
 * [new branch]      ft/bundle-2 -> ft/bundle-2

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym_Git-Exercises (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

EXERCISE 2
----------
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ ls
README.md  file.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git add .
warning: in the working copy of 'service.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git commit -m "new service.html file added"
[ft/service-redesign 723e492] new service.html file added
 1 file changed, 15 insertions(+)
 create mode 100644 service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 390 bytes | 390.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/gitarecy/Gym_Git_Exerecise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ ls
README.md  file.txt

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git add .
warning: in the working copy of 'service.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git commit -m "added service.html changes"
[main 637fb78] added service.html changes
 1 file changed, 15 insertions(+)
 create mode 100644 service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git push
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/gitarecy/Gym_Git_Exerecise-Solutions'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 626 bytes | 156.00 KiB/s, done.
From https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   53fda89..3278d5f  main       -> origin/main
Merge made by the 'ort' strategy.
 services.html | 15 +++++++++++++++
 1 file changed, 15 insertions(+)
 create mode 100644 services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 590 bytes | 590.00 KiB/s, done.
Total 5 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   3278d5f..7b48fe5  main -> main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git diff main
diff --git a/service.html b/service.html
index e36592b..4807ee2 100644
--- a/service.html
+++ b/service.html
@@ -3,7 +3,7 @@

 <HEAD>

-<TITLE>new service</TITLE>
+<TITLE>service</TITLE>

 </HEAD>

diff --git a/services.html b/services.html
deleted file mode 100644
index 5876f81..0000000
--- a/services.html
+++ /dev/null
@@ -1,15 +0,0 @@
-<!DOCTYPE html>
-<HTML>
-
-<HEAD>


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ vi service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git commit -m "kept new changes to service.html"
[ft/service-redesign 71eb597] kept new changes to service.html
 1 file changed, 1 insertion(+), 1 deletion(-)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 337 bytes | 112.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   723e492..71eb597  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git merge main
Merge made by the 'ort' strategy.
 services.html | 15 +++++++++++++++
 1 file changed, 15 insertions(+)
 create mode 100644 services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git add service.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git commit -m "Merged main branch with ft/service-redesign"
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 5 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.29 KiB | 440.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   71eb597..355342a  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.






```
