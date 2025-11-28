create an empty folder intialize git and create 3 files
SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git branch
* main

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git branch branch-1

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git branch
  branch-1
* main

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git checkout branch-1
Switched to branch 'branch-1'

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (branch-1)
$ git branch
* branch-1
  main

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (branch-1)
$ git status
On branch branch-1
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   indx.html

no changes added to commit (use "git add" and/or "git commit -a")

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (branch-1)
$ git commit -a -m "change ineer html on branch-1"
warning: in the working copy of 'indx.html', LF will be replaced by CRLF the next time Git touches it
[branch-1 6d3a0d1] change ineer html on branch-1
 1 file changed, 12 insertions(+), 1 deletion(-)

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (branch-1)
$ git log
commit 6d3a0d1a3d7f96f839c85d944b2d0dd027e98e9b (HEAD -> branch-1)
Author: Abell <habelzer@gmail.com>
Date:   Fri Nov 28 11:03:47 2025 +0300

    change ineer html on branch-1

commit 3fd78800f11f71a2b82f1b266040dee056465ed9 (main)
Author: Abell <habelzer@gmail.com>
Date:   Fri Nov 28 10:49:24 2025 +0300

    add notes

commit c40157607fc70066b42e74b951aa7642d2e44a83
Author: Abell <habelzer@gmail.com>
Date:   Fri Nov 28 10:47:27 2025 +0300

    createa index.html,style.css,readme.md and notes.txt

commit d4de1248dc68de3b78f9c8c66628bfdcc9dad368
Author: Abell <habelzer@gmail.com>
Date:   Fri Nov 28 10:28:47 2025 +0300

    correct spelling error

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (branch-1)
$ git checkout main
Switched to branch 'main'

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git merge branch-1
Updating 3fd7880..6d3a0d1
Fast-forward
 indx.html | 13 ++++++++++++-
 1 file changed, 12 insertions(+), 1 deletion(-)

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git status
On branch main
nothing to commit, working tree clean

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git branch -d branch-1
Deleted branch branch-1 (was 6d3a0d1).

SuperUser@A6E1S-PC MINGW64 ~/Desktop/A6e1/git-practice (main)
$ git branch
* main
