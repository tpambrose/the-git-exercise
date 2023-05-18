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