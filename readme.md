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
