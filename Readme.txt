$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true


- git init

- $ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.txt

nothing added to commit but untracked files present (use "git add" to track)

- $ git add test.txt

- $ git config --global user.email "asraro@gmail.com"

- $ git config --global user.name "asraro"

- $ git commit -m "initial commit"
[master (root-commit) 8901f9e] initial commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt


- $ git log
commit 8901f9e1ada17c4cda22f8c65ef5f13e58985acc (HEAD -> master)
Author: asraro <asraro@gmail.com>
Date:   Sat May 9 17:42:01 2026 -0500

    initial commit

- $ git diff test.txt
diff --git a/test.txt b/test.txt
index e69de29..ee8ef9d 100644
--- a/test.txt
+++ b/test.txt
@@ -0,0 +1 @@
+This is test file for github.
\ No newline at end of file

- Add remote origin(link your local repo to Github)

$ git remote add origin https://github.com/asraro/test-repo.git

$ git remote -v
origin  https://github.com/asraro/test-repo.git (fetch)
origin  https://github.com/asraro/test-repo.git (push)

- $ git branch -M main

- $ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 203 bytes | 101.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'main' on GitHub by visiting:
remote:      https://github.com/asraro/test-repo/pull/new/main
remote:
To https://github.com/asraro/test-repo.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

- $ git add .

- $ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   Readme.txt
        new file:   read-test.txt
        new file:   sshkey.txt
        modified:   test.txt

- Saima@DESKTOP-7FEP0Q3 MINGW64 ~/Documents/Omer/LEARN/Python/Git-Test (main)
$ git commit -m "Adding more files"
[main a391348] Adding more files
 4 files changed, 135 insertions(+)
 create mode 100644 Readme.txt
 create mode 100644 read-test.txt
 create mode 100644 sshkey.txt

- Saima@DESKTOP-7FEP0Q3 MINGW64 ~/Documents/Omer/LEARN/Python/Git-Test (main)
$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 2.06 KiB | 703.00 KiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/asraro/test-repo.git
   8901f9e..a391348  main -> main

