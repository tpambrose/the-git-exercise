PS C:\Users\Frankk\Desktop\git exercise solution> git init
Initialized empty Git repository in C:/Users/Frankk/Desktop/git exercise solution/.git/
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch master

nothing to commit (create/copy files and use "git add" to track)
PS C:\Users\Frankk\Desktop\git exercise solution> git branch -M main
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main

No commits yet

PS C:\Users\Frankk\Desktop\git exercise solution> git add readme.md
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   readme.md

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "initial commit"
PS C:\Users\Frankk\Desktop\git exercise solution> git remote add origin https://github.com/tpambrose/the-git-exercise
Enumerating objects: 3, done.
Writing objects: 100% (3/3), 209 bytes | 209.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
 * [new branch]      main -> main
PS C:\Users\Frankk\Desktop\git exercise solution> git branch Dev
PS C:\Users\Frankk\Desktop\git exercise solution> git branch list
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout Dev
Switched to branch 'Dev'
PS C:\Users\Frankk\Desktop\git exercise solution> git branch -d list    
Deleted branch list (was 9c8be1f).
* Dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'Dev' on GitHub by visiting:
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/Dev
remote:
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      Dev -> Dev
Already on 'Dev'
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin test
remote:
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/test
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      test -> test
Switched to branch 'test'
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout Dev
Switched to branch 'Dev'
PS C:\Users\Frankk\Desktop\git exercise solution> git branch -d test
Deleted branch test (was 9c8be1f).
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin Dev
Everything up-to-date
 - [deleted]         test
PS C:\Users\Frankk\Desktop\git exercise solution> git commit 
On branch Dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
PS C:\Users\Frankk\Desktop\git exercise solution>PS
        modified:   readme.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add readme.md
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch Dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   readme.md

PS C:\Users\Frankk\Desktop\git exercise solution> git commit
[Dev c79c250] PS C:\Users\Frankk\Desktop\git exercise solution>PS C:\Users\Frankk\Desktop\git exercise solution>PS C:\Users\Frankk\Desktop\git exercise solution
 1 file changed, 60 insertions(+)
PS C:\Users\Frankk\Desktop\git exercise solution> git add readme.md
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin main
Everything up-to-date

# Exercise 2
no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add readme.md
[main 4e52d87] commit
PS C:\Users\Frankk\Desktop\git exercise solution> git add home.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

PS C:\Users\Frankk\Desktop\git exercise solution> git stash save "home page"
Saved working directory and index state On main: home page
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main
nothing to commit, working tree clean
PS C:\Users\Frankk\Desktop\git exercise solution> git stash list
stash@{0}: On main: home page
PS C:\Users\Frankk\Desktop\git exercise solution> git add about.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

PS C:\Users\Frankk\Desktop\git exercise solution> git stash
Saved working directory and index state WIP on main: 4e52d87 commit
PS C:\Users\Frankk\Desktop\git exercise solution> git stash list
stash@{0}: WIP on main: 4e52d87 commit
stash@{1}: On main: home page
PS C:\Users\Frankk\Desktop\git exercise solution> git add team.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

PS C:\Users\Frankk\Desktop\git exercise solution> git stash save "team page"
Saved working directory and index state On main: team page
PS C:\Users\Frankk\Desktop\git exercise solution> git stash list
stash@{0}: On main: team page
stash@{1}: WIP on main: 4e52d87 commit
stash@{2}: On main: home page
PS C:\Users\Frankk\Desktop\git exercise solution> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --quiet           be quiet, only report errors
    --index               attempt to recreate the index
    Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git stash list
stash@{0}: On main: team page
stash@{1}: WIP on main: 4e52d87 commit
stash@{2}: On main: home page

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git stash pop stash@{1}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (a66a174a26ea4d1216e4aa8b9d4bddf41ee3f7e3)

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git stash list
stash@{0}: On main: team page
stash@{1}: On main: home page

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git stash pop stash@{1}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html 

Dropped stash@{1} (e87e70faaed9c2e77a1f61d1ab674cd76f01d929)

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git add .

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git commit -m "the about and home page"
[main 252518f] the about and home page
 2 files changed, 20 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git push --set-upstream origin main
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 1.43 KiB | 209.00 KiB/s, done.
Total 7 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/tpambrose/the-git-exercise
   9c8be1f..252518f  main -> main
branch 'main' set up to track 'origin/main'.

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$
Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$  git push --set-upstream origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.79 KiB | 916.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/tpambrose/the-git-exercise
   252518f..f474c5c  main -> main
branch 'main' set up to track 'origin/main'.

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git stash list
stash@{0}: On main: team page

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git stash pop stash@{0}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (c3ed173243482f1818a5a36ebcbbca205d66be16)

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git reset --hard
HEAD is now at f474c5c new commit

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git add --all

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git status
On branch ft/bundle-2
nothing to commit, working tree clean

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git add service.html
fatal: pathspec 'service.html' did not match any files

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git stash list

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git commit -m "update"
On branch ft/bundle-2
nothing to commit, working tree clean

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git push --set upstream origin ft/bundle-2
error: src refspec origin does not match any
error: failed to push some refs to 'upstream'

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (ft/bundle-2)
$ git push origin ft/bundle-2
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/ft/bundle-2
remote:
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      ft/bundle-2 -> ft/bundle-2

# Bundle 2
# Exercise 1
Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git branch ft/bundle-2

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git branch
  Dev
  ft/bundle-2
* main

Frankk@Frank MINGW64 ~/Desktop/git exercise solution (main)
$ git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/bundle-2
Switched to branch 'ft/bundle-2'
PS C:\Users\Frankk\Desktop\git exercise solution> git status
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        SERVICE.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
  (use "git restore --staged <file>..." to unstage)
        new file:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution>
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "update service in ft/bundle-2"
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 SERVICE.html
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Writing objects: 100% (6/6), 916 bytes | 458.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
To https://github.com/tpambrose/the-git-exercise
   d8809a9..31f7b47  ft/bundle-2 -> ft/bundle-2
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
error: Your local changes to the following files would be overwritten by checkout:
        SERVICE.html
Please commit your changes or stash them before you switch branches.
error: The following untracked working tree files would be overwritten by checkout:
        service.html
Please move or remove them before you switch branches.
Aborting
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/bundle-2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/bundle-2
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "new service update"
[ft/bundle-2 8415e98] new service update
 1 file changed, 10 insertions(+)
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 584 bytes | 292.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/tpambrose/the-git-exercise
   d8809a9..d38c950  main -> main
PS C:\Users\Frankk\Desktop\git exercise solution>

# Exercise 2

PS C:\Users\Frankk\Desktop\git exercise solution> git pull origin main
From https://github.com/tpambrose/the-git-exercise
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Already on 'main'
M       SERVICE.html
M       service.html
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git add --all 
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "updated commit"
[main a9be1d7] updated commit
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 408 bytes | 136.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/tpambrose/the-git-exercise
   0879a6b..a9be1d7  main -> main
PS C:\Users\Frankk\Desktop\git exercise solution> git pull origin main
From https://github.com/tpambrose/the-git-exercise
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution>                        
 *  History restored 

Switched to a new branch 'ft/service-redesign'
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git add --all
PS C:\Users\Frankk\Desktop\git exercise solution> gti status
gti : The term 'gti' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name,   
or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ gti status
+ ~~~
    + FullyQualifiedErrorId : CommandNotFoundException
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git SERVICE.htm
PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html
no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
M       SERVICE.html
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\Frankk\Desktop\git exercise solution> git pull origin main
remote: Enumerating objects: 8, done.
remote: Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), 1.30 KiB | 5.00 KiB/s, done.
From https://github.com/tpambrose/the-git-exercise
 * branch            main       -> FETCH_HEAD
   a9be1d7..4a26e15  main       -> origin/main
Updating a9be1d7..4a26e15
Fast-forward
 readme.md | 51 ++++++++++++++++++++++++++++++++++++++++++++++++++-
 1 file changed, 50 insertions(+), 1 deletion(-)
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "service update"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

On branch main
Your branch is up to date with 'origin/main'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/service-redesign
M       SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> gti status
gti : The term 'gti' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name,   
or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ gti status
+ ~~~
    + FullyQualifiedErrorId : CommandNotFoundException
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add --all
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "ft/service-redesign"
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "updating new changes to service page"
 1 file changed, 3 insertions(+), 6 deletions(-)
PS C:\Users\Frankk\Desktop\git exercise solution> git push 
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Frankk\Desktop\git exercise solution>  git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 338 bytes | 338.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/ft/service-redesign
remote:
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
M       SERVICE.html
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   service.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main

Changes to be committed:
        modified:   service.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "changes is service page"
[main ce57295] changes is service page
PS C:\Users\Frankk\Desktop\git exercise solution> git push
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
To https://github.com/tpambrose/the-git-exercise
   4a26e15..ce57295  main -> main
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout -b ft/service-redesign
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
M       SERVICE.html
Your branch is up to date with 'origin/ft/service-redesign'.
Already up to date.
Auto-merging service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
error: Merging is not possible because you have unmerged files.
hint: as appropriate to mark resolution and make a commit.
PS C:\Users\Frankk\Desktop\git exercise solution> git add/rm service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git add service html
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
Please, commit your changes before you merge.
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "service page update "
[ft/service-redesign 2e6ec36] service page update
PS C:\Users\Frankk\Desktop\git exercise solution> git merge 
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
M       SERVICE.html
Your branch is ahead of 'origin/ft/service-redesign' by 7 commits.
  (use "git push" to publish your local commits)
PS C:\Users\Frankk\Desktop\git exercise solution> git diff main
diff --git a/service.html b/service.html
index 38ddcea..9e8797d 100644
+++ b/service.html
@@ -3,16 +3,8 @@
 <head>
     <title>service</title>
 </head>
 <body>
     <h1>Welcome to my service page!</h1>
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "latest update"
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 7 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
PS C:\Users\Frankk\Desktop\git exercise solution> git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 250 bytes | 250.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/tpambrose/the-git-exercise
   0c6b076..2e6ec36  ft/service-redesign -> ft/service-redesign
PS C:\Users\Frankk\Desktop\git exercise solution> ft/service-redesign
 # Bundle 3
 # exercise 1 $ 2
 PS C:\Users\Frankk\Desktop\git exercise solution> git pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.      

PS C:\Users\Frankk\Desktop\git exercise solution> git pull origin main
From https://github.com/tpambrose/the-git-exercise
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Already on 'main'
M       SERVICE.html
M       service.html
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git add --all 
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "updated commit"
[main a9be1d7] updated commit
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin main
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 408 bytes | 136.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/tpambrose/the-git-exercise
   0879a6b..a9be1d7  main -> main
PS C:\Users\Frankk\Desktop\git exercise solution> git pull origin main
From https://github.com/tpambrose/the-git-exercise
 * branch            main       -> FETCH_HEAD
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution>                        
 *  History restored 

Switched to a new branch 'ft/service-redesign'
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git add --all
PS C:\Users\Frankk\Desktop\git exercise solution> gti status
gti : The term 'gti' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name,   
or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ gti status
+ ~~~
    + FullyQualifiedErrorId : CommandNotFoundException
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git SERVICE.htm
PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html
no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
M       SERVICE.html
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git pull main
fatal: 'main' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
PS C:\Users\Frankk\Desktop\git exercise solution> git pull origin main
remote: Enumerating objects: 8, done.
remote: Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), 1.30 KiB | 5.00 KiB/s, done.
From https://github.com/tpambrose/the-git-exercise
 * branch            main       -> FETCH_HEAD
   a9be1d7..4a26e15  main       -> origin/main
Updating a9be1d7..4a26e15
Fast-forward
 readme.md | 51 ++++++++++++++++++++++++++++++++++++++++++++++++++-
 1 file changed, 50 insertions(+), 1 deletion(-)
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "service update"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

On branch main
Your branch is up to date with 'origin/main'.
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/service-redesign
M       SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> gti status
gti : The term 'gti' is not recognized as the name of a cmdlet, function, script file, or operable program. Check the spelling of the name,   
or if a path was included, verify that the path is correct and try again.
At line:1 char:1
+ gti status
+ ~~~
    + FullyQualifiedErrorId : CommandNotFoundException
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add --all
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "ft/service-redesign"
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "updating new changes to service page"
 1 file changed, 3 insertions(+), 6 deletions(-)
PS C:\Users\Frankk\Desktop\git exercise solution> git push 
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Frankk\Desktop\git exercise solution>  git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 338 bytes | 338.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/ft/service-redesign
remote:
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
M       SERVICE.html
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   service.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git add SERVICE.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main

Changes to be committed:
        modified:   service.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   SERVICE.html

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "changes is service page"
[main ce57295] changes is service page
PS C:\Users\Frankk\Desktop\git exercise solution> git push
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
To https://github.com/tpambrose/the-git-exercise
   4a26e15..ce57295  main -> main
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout -b ft/service-redesign
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
M       SERVICE.html
Your branch is up to date with 'origin/ft/service-redesign'.
Already up to date.
Auto-merging service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
error: Merging is not possible because you have unmerged files.
hint: as appropriate to mark resolution and make a commit.
PS C:\Users\Frankk\Desktop\git exercise solution> git add/rm service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git add service html
PS C:\Users\Frankk\Desktop\git exercise solution> git add service.html
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
Please, commit your changes before you merge.
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "service page update "
[ft/service-redesign 2e6ec36] service page update
PS C:\Users\Frankk\Desktop\git exercise solution> git merge 
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
M       SERVICE.html
Your branch is ahead of 'origin/ft/service-redesign' by 7 commits.
  (use "git push" to publish your local commits)
PS C:\Users\Frankk\Desktop\git exercise solution> git diff main
diff --git a/service.html b/service.html
index 38ddcea..9e8797d 100644
+++ b/service.html
@@ -3,16 +3,8 @@
 <head>
     <title>service</title>
 </head>
 <body>
     <h1>Welcome to my service page!</h1>
PS C:\Users\Frankk\Desktop\git exercise solution> git merge main
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "latest update"
On branch ft/service-redesign
Your branch is ahead of 'origin/ft/service-redesign' by 7 commits.
  (use "git push" to publish your local commits)

PS C:\Users\Frankk\Desktop\git exercise solution> git push
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/tpambrose/the-git-exercise
PS C:\Users\Frankk\Desktop\git exercise solution> git push
PS C:\Users\Frankk\Desktop\git exercise solution> git pull 
From https://github.com/tpambrose/the-git-exercise
   e3c6dd7..0c9f725  ft/bundle-2 -> origin/ft/bundle-2
Already up to date.
Switched to branch 'main'
M       readme.md
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git pull
Already up to date.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
M       SERVICE.html
M       readme.md
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin
Enumerating objects: 5, done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.96 KiB | 669.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/tpambrose/the-git-exercise
   2e6ec36..cc71c69  ft/service-redesign -> ft/service-redesign
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git pull
remote: Enumerating objects: 2, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 0), reused 0 (delta 0), pack-reused 0
From https://github.com/tpambrose/the-git-exercise
Fast-forward
 readme.md    | 261 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 service.html |   8 --
 2 files changed, 260 insertions(+), 9 deletions(-)
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/team-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "new team.html page"
[ft/team-page 3bcc1fc] new team.html page
 1 file changed, 15 insertions(+)
 create mode 100644 team.html
PS C:\Users\Frankk\Desktop\git exercise solution> git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 419 bytes | 209.00 KiB/s, done.
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      ft/team-page -> ft/team-page
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Frankk\Desktop\git exercise solution> git log
Author: teta <tpambrose0@example.com>


commit 70b4ef4cfd5ecae2ff9157a5240ad8b4baa14526 (origin/main, main, ft/contact-page)
Merge: a1a9416 cc71c69
Author: Teta Precious <110498537+tpambrose@users.noreply.github.com>
Date:   Sat May 20 13:39:37 2023 +0000

PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/team-page
Switched to branch 'ft/team-page'
PS C:\Users\Frankk\Desktop\git exercise solution> git log
Author: teta <tpambrose0@example.com>

    new team.html page

commit 70b4ef4cfd5ecae2ff9157a5240ad8b4baa14526 (origin/main, main, ft/contact-page)
Author: Teta Precious <110498537+tpambrose@users.noreply.github.com>

PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/contact-page
Switched to branch 'ft/contact-page'
PS C:\Users\Frankk\Desktop\git exercise solution> git cherry- pick commit 3bcc1fc282510bdae6aaee75c62a007284b80fed
The most similar command is
        cherry
PS C:\Users\Frankk\Desktop\git exercise solution> git cherry-pick commit 3bcc1fc282510bdae6aaee75c62a007284b80fed
PS C:\Users\Frankk\Desktop\git exercise solution> git cherry-pick 3bcc1fc282510bdae6aaee75c62a007284b80fed       
[ft/contact-page 3f9e054] new team.html page
 Date: Sat May 20 13:48:06 2023 +0000
 1 file changed, 15 insertions(+)
 create mode 100644 team.html
PS C:\Users\Frankk\Desktop\git exercise solution> git add contact.html
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "contact page "
[ft/contact-page e0a5aa7] contact page
 create mode 100644 contact.html
PS C:\Users\Frankk\Desktop\git exercise solution> git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Frankk\Desktop\git exercise solution> git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Writing objects: 100% (6/6), 759 bytes | 151.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote:
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/ft/contact-page
To https://github.com/tpambrose/the-git-exercise
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/contact-page
Already on 'ft/contact-page'
Your branch is up to date with 'origin/ft/contact-page'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/faq-page
error: pathspec 'ft/faq-page' did not match any file(s) known to git
PS C:\Users\Frankk\Desktop\git exercise solution> git add fag.html
fatal: pathspec 'fag.html' did not match any files
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/faq-page
Untracked files:
        faq.html

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/faq-page
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   faq.html

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "add new file faq.html"
[ft/faq-page 837b98a] add new file faq.html
 create mode 100644 faq.html
PS C:\Users\Frankk\Desktop\git exercise solution> git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Frankk\Desktop\git exercise solution>  git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Writing objects: 100% (3/3), 383 bytes | 127.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/ft/faq-page
remote:
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.
PS C:\Users\Frankk\Desktop\git exercise solution> git log 

Author: teta <tpambrose0@example.com>
Date:   Sat May 20 14:16:10 2023 +0000


commit e0a5aa75d55da9d20e5975a831102b1ba2c27ea3 (origin/ft/contact-page, ft/contact-page)
Author: teta <tpambrose0@example.com>
Date:   Sat May 20 14:04:01 2023 +0000

    contact page
PS C:\Users\Frankk\Desktop\git exercise solution> git revert 3bcc1fc282510bdae6aaee75c62a007284b80fed
[ft/faq-page f5c0eed] Revert "new team.html page"
 1 file changed, 15 deletions(-)
 delete mode 100644 team.html
PS C:\Users\Frankk\Desktop\git exercise solution> git log
Author: teta <tpambrose0@example.com>
Date:   Sat May 20 14:22:14 2023 +0000

    Revert "new team.html page"

    This reverts commit 3bcc1fc282510bdae6aaee75c62a007284b80fed.

commit 837b98a928f22e4cde516de44e593983c02aa518 (origin/ft/faq-page)
Author: teta <tpambrose0@example.com>
PS C:\Users\Frankk\Desktop\git exercise solution> git push
Enumerating objects: 3, done.
Delta compression using up to 4 threads
Writing objects: 100% (2/2), 270 bytes | 270.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
   837b98a..f5c0eed  ft/faq-page -> ft/faq-page
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/faq-page
Already on 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout main
Your branch is up to date with 'origin/main'.
PS C:\Users\Frankk\Desktop\git exercise solution> git add home.html
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   home.html

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "the changes made in main"
PS C:\Users\Frankk\Desktop\git exercise solution> git push 
To https://github.com/tpambrose/the-git-exercise
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/tpambrose/the-git-exercise'
hint: Updates were rejected because the remote contains work that you do
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\Frankk\Desktop\git exercise solution> git add --all
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\Frankk\Desktop\git exercise solution> git push
To https://github.com/tpambrose/the-git-exercise
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/tpambrose/the-git-exercise'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS C:\Users\Frankk\Desktop\git exercise solution> git push --help
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 637 bytes | 12.00 KiB/s, done.
From https://github.com/tpambrose/the-git-exercise
   70b4ef4..7cd5410  main       -> origin/main
 team.html | 15 +++++++++++++++
 1 file changed, 15 insertions(+)
 create mode 100644 team.html
PS C:\Users\Frankk\Desktop\git exercise solution> git add --all
PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "update "
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

PS C:\Users\Frankk\Desktop\git exercise solution> git push 
Counting objects: 100% (8/8), done.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 569 bytes | 569.00 KiB/s, done.
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/tpambrose/the-git-exercise
   7cd5410..a65d31e  main -> main
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout -b ft/home-page-redesign
fatal: a branch named 'ft/home-page-redesign' already exists
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/home-page-redesign
nothing to commit, working tree clean
PS C:\Users\Frankk\Desktop\git exercise solution> git log
Date:   Sat May 20 14:22:14 2023 +0000
    Revert "new team.html page"

    This reverts commit 3bcc1fc282510bdae6aaee75c62a007284b80fed.

Author: teta <tpambrose0@example.com>
Date:   Sat May 20 14:16:10 2023 +0000
PS C:\Users\Frankk\Desktop\git exercise solution> git checkout ft/home-page-redesign
Already on 'ft/home-page-redesign'
PS C:\Users\Frankk\Desktop\git exercise solution> git rebase main
warning: skipped previously applied commit 3f9e054
hint: use --reapply-cherry-picks to include skipped commits
hint: Disable this message with "git config advice.skippedCherryPicks false"
Successfully rebased and updated refs/heads/ft/home-page-redesign.
nothing to commit, working tree clean
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
        modified:   home.html

PS C:\Users\Frankk\Desktop\git exercise solution> git add home.html
PS C:\Users\Frankk\Desktop\git exercise solution> git status
On branch ft/home-page-redesign
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   home.html

PS C:\Users\Frankk\Desktop\git exercise solution> git commit -m "new changes to home page"
 1 file changed, 3 insertions(+)
PS C:\Users\Frankk\Desktop\git exercise solution> git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS C:\Users\Frankk\Desktop\git exercise solution>  git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 4 threads
Compressing objects: 100% (11/11), done.
Writing objects: 100% (11/11), 1.17 KiB | 299.00 KiB/s, done.
Total 11 (delta 6), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (6/6), completed with 2 local objects.
remote: 
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/tpambrose/the-git-exercise/pull/new/ft/home-page-redesign
remote:
To https://github.com/tpambrose/the-git-exercise
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.