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