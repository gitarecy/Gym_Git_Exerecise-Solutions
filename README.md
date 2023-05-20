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
```
BUNDLE 3
--------
EXERCISE 1
----------
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$ vi team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$ git add .
warning: in the working copy of 'team.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$ git commit -m "Added team.html"
[ft/team-page 454fab3] Added team.html
 1 file changed, 15 insertions(+)
 create mode 100644 team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 337 bytes | 337.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/gitarecy/Gym_Git_Exerecise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git commit -m "created new branch"
On branch ft/contact-page
nothing to commit, working tree clean

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$ git log
commit 454fab3480254922549aef27d1a957ef11371f7e (HEAD -> ft/team-page, origin/ft/team-page)
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 09:57:16 2023 +0200

    Added team.html

commit 482be4329ad367c73226e68263cc8f760979ed7a (origin/main, main, ft/contact-page)
Merge: 4449ea0 299f89f
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 09:29:36 2023 +0200

    Merge branch 'main' of https://github.com/gitarecy/Gym_Git_Exerecise-Solutions

commit 4449ea0944c7ebdaf89a681a4b82aede1a88d32e
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 09:29:23 2023 +0200

    updates on readme

commit 299f89f92cca0ec55456ff98b3d5baec6dafaa44
Merge: 7b48fe5 71eb597
Author: gitarecy <98228087+gitarecy@users.noreply.github.com>


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git cherry-pick 454fab3480254922549aef27d1a957ef11371f7e
[ft/contact-page 2ed6f1a] Added team.html
 Date: Sat May 20 09:57:16 2023 +0200
 1 file changed, 15 insertions(+)
 create mode 100644 team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ nano contact.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ vi contact.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git add .
warning: in the working copy of 'contact.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git commit -m "Added contact.html page"
[ft/contact-page c5e0236] Added contact.html page
 1 file changed, 15 insertions(+)
 create mode 100644 contact.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 582 bytes | 291.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/gitarecy/Gym_Git_Exerecise-Solutions/pull/new/ft/contact-page
remote:
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ vi faq.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git add .
warning: in the working copy of 'faq.html', LF will be replaced by CRLF the next time Git touches it

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git commit -m "added faq page"
[ft/faq-page 58a2be4] added faq page
 1 file changed, 15 insertions(+)
 create mode 100644 faq.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 332 bytes | 332.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/gitarecy/Gym_Git_Exerecise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git log
commit 58a2be474fd69407735b1e946b876a489839f861 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 10:53:04 2023 +0200

    added faq page

commit c5e0236336928a782e336ada57fd3758276c6c31 (origin/ft/contact-page, ft/contact-page)
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 10:49:57 2023 +0200

    Added contact.html page

commit 2ed6f1a056ff9a42ca438f10ce194b8613ae5eb0
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 09:57:16 2023 +0200

    Added team.html

commit 482be4329ad367c73226e68263cc8f760979ed7a (origin/main, main)
Merge: 4449ea0 299f89f
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 09:29:36 2023 +0200

:
commit 58a2be474fd69407735b1e946b876a489839f861 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 10:53:04 2023 +0200

    added faq page

commit c5e0236336928a782e336ada57fd3758276c6c31 (origin/ft/contact-page, ft/contact-page)
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 10:49:57 2023 +0200

    Added contact.html page

commit 2ed6f1a056ff9a42ca438f10ce194b8613ae5eb0
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 09:57:16 2023 +0200

    Added team.html

commit 482be4329ad367c73226e68263cc8f760979ed7a (origin/main, main)
Merge: 4449ea0 299f89f
Author: gitarecy <gitarecynthia@gmail.com>
Date:   Sat May 20 09:29:36 2023 +0200

    Merge branch 'main' of https://github.com/gitarecy/Gym_Git_Exerecise-Solutions


LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git revert 454fab3480254922549aef27d1a957ef11371f7e
[ft/faq-page b6fa313] Revert "Added team.html"
 1 file changed, 15 deletions(-)
 delete mode 100644 team.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git commit -m "revert changes of the last commit of the ft/team-page"
On branch ft/faq-page
Your branch is ahead of 'origin/ft/faq-page' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 270 bytes | 270.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   58a2be4..b6fa313  ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)


EXERCISE 2
----------
LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ ls
README.md  file.txt  service.html  services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git pull
remote: Enumerating objects: 13, done.
remote: Counting objects: 100% (13/13), done.
remote: Compressing objects: 100% (8/8), done.
Unpacking objects: 100% (8/8), 2.60 KiB | 78.00 KiB/s, done.
remote: Total 8 (delta 4), reused 0 (delta 0), pack-reused 0
From https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   482be43..82cdbf5  main       -> origin/main
Updating 482be43..82cdbf5
Fast-forward
 about.html   | 15 +++++++++++++++
 contact.html | 15 +++++++++++++++
 faq.html     | 15 +++++++++++++++
 home.html    | 15 +++++++++++++++
 4 files changed, 60 insertions(+)
 create mode 100644 about.html
 create mode 100644 contact.html
 create mode 100644 faq.html
 create mode 100644 home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git push
Everything up-to-date

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git commit -m "update main"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git push
Everything up-to-date

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ ls
README.md   contact.html  file.txt   service.html
about.html  faq.html      home.html  services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ vi home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git commit -m "changes to home.html"
[main 4989ce3] changes to home.html
 1 file changed, 1 insertion(+), 1 deletion(-)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 332 bytes | 332.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
   82cdbf5..4989ce3  main -> main

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)
$ ls
README.md   contact.html  file.txt   service.html
about.html  faq.html      home.html  services.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)
$ vi home.html

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)
$ git add .

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)
$ git commit -m "Changes to home page"
[ft/home-page-redesign 36890ce] Changes to home page
 1 file changed, 1 insertion(+), 1 deletion(-)

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)
$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 287 bytes | 287.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/gitarecy/Gym_Git_Exerecise-Solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/gitarecy/Gym_Git_Exerecise-Solutions
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

LENOVO@DESKTOP-5GQ3HIK MINGW64 ~/Gym-git-exercise (ft/home-page-redesign)


```
