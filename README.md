C:\Users\vitsin\Documents\git\test_git\devops-netology>mkdir branching

C:\Users\vitsin\Documents\git\test_git\devops-netology>cd branching

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad merge.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>cd ..

C:\Users\vitsin\Documents\git\test_git\devops-netology>git status
HEAD detached from origin/main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .idea/
        branching/

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\vitsin\Documents\git\test_git\devops-netology>git add branching/*

C:\Users\vitsin\Documents\git\test_git\devops-netology>git status
HEAD detached from origin/main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   branching/merge.sh
        new file:   branching/rebase.sh

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .idea/


C:\Users\vitsin\Documents\git\test_git\devops-netology>git commit -m "prepare for merge and rebase"
[detached HEAD 52b2226] prepare for merge and rebase
 2 files changed, 16 insertions(+)
 create mode 100644 branching/merge.sh
 create mode 100644 branching/rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology>git branch
* (HEAD detached from origin/main)
  exp
  fix
  main

C:\Users\vitsin\Documents\git\test_git\devops-netology>git remote
bitbucket
gitlab
origin

C:\Users\vitsin\Documents\git\test_git\devops-netology>git push origin
fatal: You are not currently on a branch.
To push the history leading to the current (detached HEAD)
state now, use

    git push origin HEAD:<name-of-remote-branch>


C:\Users\vitsin\Documents\git\test_git\devops-netology>git checkout main
Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  52b2226 prepare for merge and rebase

If you want to keep it by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> 52b2226

Switched to branch 'main'
Your branch is up to date with 'origin/main'.

C:\Users\vitsin\Documents\git\test_git\devops-netology>git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .idea/

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\vitsin\Documents\git\test_git\devops-netology>git log --graph
* commit 16ca2292b1b060b30265d39cc295d6c732b90c6d (HEAD -> main, tag: v0.1, tag: v0.0, origin/main, origin/HEAD, gitlab/main, bitbucket/main)
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Thu Jul 15 14:26:40 2021 +0300
|
|     before push
|
* commit 5491f27f241ce30d678f4e1bcfad08840d8060a6
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:37:15 2021 +0300
|
|     help for git & git add
|
* commit b438fb10a9aaa5aa85378d316a55f7eda464a8a3
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:29:40 2021 +0300
|
|     Moved and deleted
|
* commit d47c68a17546655e253b3e1fff1fa1ca933f4dfd
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:27:23 2021 +0300
|
|     prepare to delete and move
|
* commit 5edc0c65080093692950e7adf2ae23d09883f06a
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:23:57 2021 +0300
|
|     Added gitignore
|
* commit b561454a62a021e5cd15a3d4baf673a8ddabae78
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:06:39 2021 +0300
|
|     first commit
|
* commit 511b14da26901c2ad7c54d47fef6f7da99a14faa
  Author: vitsinv <79792682+vitsinv@users.noreply.github.com>
  Date:   Mon Jul 12 18:52:40 2021 +0300

      Initial commit

C:\Users\vitsin\Documents\git\test_git\devops-netology>cd
C:\Users\vitsin\Documents\git\test_git\devops-netology

C:\Users\vitsin\Documents\git\test_git\devops-netology>dir
 Том в устройстве C имеет метку Windows
 Серийный номер тома: A64B-8ACC

 Содержимое папки C:\Users\vitsin\Documents\git\test_git\devops-netology

19.07.2021  19:46    <DIR>          .
19.07.2021  19:46    <DIR>          ..
12.07.2021  19:08                40 .gitignore
19.07.2021  19:41    <DIR>          .idea
16.07.2021  13:10                13 has_been_moved.txt
19.07.2021  19:46            18 029 README.md
16.07.2021  13:10    <DIR>          terraform
               3 файлов         18 082 байт
               4 папок  193 127 161 856 байт свободно

C:\Users\vitsin\Documents\git\test_git\devops-netology>git checkout exp
Switched to branch 'exp'

C:\Users\vitsin\Documents\git\test_git\devops-netology>dir
 Том в устройстве C имеет метку Windows
 Серийный номер тома: A64B-8ACC

 Содержимое папки C:\Users\vitsin\Documents\git\test_git\devops-netology

19.07.2021  19:47    <DIR>          .
19.07.2021  19:47    <DIR>          ..
12.07.2021  19:08                40 .gitignore
19.07.2021  19:41    <DIR>          .idea
16.07.2021  13:10                13 has_been_moved.txt
19.07.2021  19:47                23 README.md
16.07.2021  13:10    <DIR>          terraform
               3 файлов             76 байт
               4 папок  193 127 182 336 байт свободно

C:\Users\vitsin\Documents\git\test_git\devops-netology>git checkout fix
Switched to branch 'fix'
Your branch is up to date with 'origin/fix'.

C:\Users\vitsin\Documents\git\test_git\devops-netology>dir
 Том в устройстве C имеет метку Windows
 Серийный номер тома: A64B-8ACC

 Содержимое папки C:\Users\vitsin\Documents\git\test_git\devops-netology

19.07.2021  19:48    <DIR>          .
19.07.2021  19:48    <DIR>          ..
12.07.2021  19:08                40 .gitignore
19.07.2021  19:41    <DIR>          .idea
19.07.2021  19:48             1 411 README.md
19.07.2021  19:48    <DIR>          terraform
19.07.2021  19:48                15 will_be_deleted.txt
19.07.2021  19:48                54 will_be_moved.txt
               4 файлов          1 520 байт
               4 папок  193 126 785 024 байт свободно

C:\Users\vitsin\Documents\git\test_git\devops-netology>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

C:\Users\vitsin\Documents\git\test_git\devops-netology>mkdir branching

C:\Users\vitsin\Documents\git\test_git\devops-netology>cd branching

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>dir
 Том в устройстве C имеет метку Windows
 Серийный номер тома: A64B-8ACC

 Содержимое папки C:\Users\vitsin\Documents\git\test_git\devops-netology\branching

19.07.2021  19:49    <DIR>          .
19.07.2021  19:49    <DIR>          ..
               0 файлов              0 байт
               2 папок  193 126 432 768 байт свободно

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad merge.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../.idea/
        ./

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>cd ..

C:\Users\vitsin\Documents\git\test_git\devops-netology>git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .idea/
        branching/

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\vitsin\Documents\git\test_git\devops-netology>git add branching/

C:\Users\vitsin\Documents\git\test_git\devops-netology>git commit -m "prepare for merge and rebase"
[main dad3773] prepare for merge and rebase
 2 files changed, 16 insertions(+)
 create mode 100644 branching/merge.sh
 create mode 100644 branching/rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology>git remote
bitbucket
gitlab
origin

C:\Users\vitsin\Documents\git\test_git\devops-netology>git push origin
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 459 bytes | 459.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/vitsinv/devops-netology/
   16ca229..dad3773  main -> main

C:\Users\vitsin\Documents\git\test_git\devops-netology>git branch
  exp
  fix
* main

C:\Users\vitsin\Documents\git\test_git\devops-netology>git checkout -b git-merge
Switched to a new branch 'git-merge'

C:\Users\vitsin\Documents\git\test_git\devops-netology>git branch
  exp
  fix
* git-merge
  main

C:\Users\vitsin\Documents\git\test_git\devops-netology>notepad /branching/merge.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology>cd branching

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad merge.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git status
On branch git-merge
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   merge.sh

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../.idea/

no changes added to commit (use "git add" and/or "git commit -a")

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git add merge.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git commit -m "merge: @ instead *"
[git-merge 2ad18d0] merge: @ instead *
 1 file changed, 2 insertions(+), 2 deletions(-)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push origin
fatal: The current branch git-merge has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin git-merge


C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git branch
  exp
  fix
* git-merge
  main

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push --set-upstream origin git-merge
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 388 bytes | 388.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'git-merge' on GitHub by visiting:
remote:      https://github.com/vitsinv/devops-netology/pull/new/git-merge
remote:
To https://github.com/vitsinv/devops-netology/
 * [new branch]      git-merge -> git-merge
Branch 'git-merge' set up to track remote branch 'git-merge' from 'origin'.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git log --graph --all
* commit 2ad18d0c068c0d31275fc5c6f6eb76c5bfc60db7 (HEAD -> git-merge, origin/git-merge)
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 19 19:55:46 2021 +0300
|
|     merge: @ instead *
|
* commit dad37735803fcc458d7eb55c23716734371c66e3 (origin/main, origin/HEAD, main)
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 19 19:51:17 2021 +0300
|
|     prepare for merge and rebase
|
| * commit e7ad8614b5577ededd9e4091ba3de326a985f606 (exp)
|/  Author: Viktor Vinogradov <v.vitsin@gmail.com>
|   Date:   Mon Jul 19 18:51:07 2021 +0300
|
|       test in exp branch
|
* commit 16ca2292b1b060b30265d39cc295d6c732b90c6d (tag: v0.1, tag: v0.0, gitlab/main, bitbucket/main)
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Thu Jul 15 14:26:40 2021 +0300
|
|     before push
|
* commit 5491f27f241ce30d678f4e1bcfad08840d8060a6
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:37:15 2021 +0300
|
|     help for git & git add
|
* commit b438fb10a9aaa5aa85378d316a55f7eda464a8a3
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:29:40 2021 +0300
|
|     Moved and deleted
|
| * commit 3c2c5b667d3a600eb83856ed8ecf48353c69c186 (origin/fix, fix)
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Thu Jul 15 16:24:51 2021 +0300
| |
| |     Second Update with Pycharm
| |
| * commit 392f696ffc11f82e69c9f2aeabcd11ad181befc2
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Thu Jul 15 16:22:42 2021 +0300
| |
| |     Updated with Pycharm
| |
| * commit 5c5891d0b81dbcef5de00be71abcce2923f6ceed
|/  Author: Viktor Vinogradov <v.vitsin@gmail.com>
|   Date:   Thu Jul 15 16:03:55 2021 +0300

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad merge.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git add merge.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git commit -m "merge: use shift"
[git-merge fc70f70] merge: use shift
 1 file changed, 3 insertions(+), 2 deletions(-)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push origin
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 463 bytes | 463.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/vitsinv/devops-netology/
   2ad18d0..fc70f70  git-merge -> git-merge

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   rebase.sh

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../.idea/

no changes added to commit (use "git add" and/or "git commit -a")

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git add rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git commit -m "change rebase.sh"
[main b42d05e] change rebase.sh
 1 file changed, 5 insertions(+), 3 deletions(-)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push origin
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 398 bytes | 398.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/vitsinv/devops-netology/
   dad3773..b42d05e  main -> main

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git log --oneline
b42d05e (HEAD -> main, origin/main, origin/HEAD) change rebase.sh
dad3773 prepare for merge and rebase
16ca229 (tag: v0.1, tag: v0.0, gitlab/main, bitbucket/main) before push
5491f27 help for git & git add
b438fb1 Moved and deleted
d47c68a prepare to delete and move
5edc0c6 Added gitignore
b561454 first commit
511b14d Initial commit

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git checkout dad3773
Note: switching to 'dad3773'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at dad3773 prepare for merge and rebase

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git-rebase
"git-rebase" не является внутренней или внешней
командой, исполняемой программой или пакетным файлом.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git rebase
You are not currently on a branch.
Please specify which branch you want to rebase against.
See git-rebase(1) for details.

    git rebase '<branch>'


C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git branch
* (HEAD detached at dad3773)
  exp
  fix
  git-merge
  main

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git rebase dad3773
HEAD is up to date.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git log --graph --all
* commit b42d05e90e2be9799606ac72c025f358ccd929ff (origin/main, origin/HEAD, main)
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 19 20:03:05 2021 +0300
|
|     change rebase.sh
|
| * commit fc70f700cead97ac159e05d4c62c98bb8335a83c (origin/git-merge, git-merge)
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Mon Jul 19 20:01:21 2021 +0300
| |
| |     merge: use shift
| |
| * commit 2ad18d0c068c0d31275fc5c6f6eb76c5bfc60db7
|/  Author: Viktor Vinogradov <v.vitsin@gmail.com>
|   Date:   Mon Jul 19 19:55:46 2021 +0300
|
|       merge: @ instead *
|
* commit dad37735803fcc458d7eb55c23716734371c66e3 (HEAD)
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 19 19:51:17 2021 +0300
|
|     prepare for merge and rebase
|
| * commit e7ad8614b5577ededd9e4091ba3de326a985f606 (exp)
|/  Author: Viktor Vinogradov <v.vitsin@gmail.com>
|   Date:   Mon Jul 19 18:51:07 2021 +0300
|
|       test in exp branch
|
* commit 16ca2292b1b060b30265d39cc295d6c732b90c6d (tag: v0.1, tag: v0.0, gitlab/main, bitbucket/main)
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Thu Jul 15 14:26:40 2021 +0300
|
|     before push
|
* commit 5491f27f241ce30d678f4e1bcfad08840d8060a6
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:37:15 2021 +0300
|
|     help for git & git add
|
* commit b438fb10a9aaa5aa85378d316a55f7eda464a8a3
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 12 19:29:40 2021 +0300
|
|     Moved and deleted
|
| * commit 3c2c5b667d3a600eb83856ed8ecf48353c69c186 (origin/fix, fix)
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Thu Jul 15 16:24:51 2021 +0300

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git status
HEAD detached at dad3773
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   rebase.sh

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        ../.idea/

no changes added to commit (use "git add" and/or "git commit -a")

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git add rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git commit -m "git-rebase 1"
[detached HEAD 10a2200] git-rebase 1
 1 file changed, 5 insertions(+), 3 deletions(-)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push origin git-rebase
error: src refspec git-rebase does not match any
error: failed to push some refs to 'https://github.com/vitsinv/devops-netology/'

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git restore
fatal: you must specify path(s) to restore

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git branch
* (HEAD detached from dad3773)
  exp
  fix
  git-merge
  main

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git reset --HARD HEAD~1
error: unknown option `HARD'
usage: git reset [--mixed | --soft | --hard | --merge | --keep] [-q] [<commit>]
   or: git reset [-q] [<tree-ish>] [--] <pathspec>...
   or: git reset [-q] [--pathspec-from-file [--pathspec-file-nul]] [<tree-ish>]
   or: git reset --patch [<tree-ish>] [--] [<pathspec>...]
   or: DEPRECATED: git reset [-q] [--stdin [-z]] [<tree-ish>]

    -q, --quiet           be quiet, only report errors
    --mixed               reset HEAD and index
    --soft                reset only HEAD
    --hard                reset HEAD, index and working tree
    --merge               reset HEAD, index and working tree
    --keep                reset HEAD but keep local changes
    --recurse-submodules[=<reset>]
                          control recursive updating of submodules
    -p, --patch           select hunks interactively
    -N, --intent-to-add   record only the fact that removed paths will be added later
    --pathspec-from-file <file>
                          read pathspec from file
    --pathspec-file-nul   with --pathspec-from-file, pathspec elements are separated with NUL character
    -z                    DEPRECATED (use --pathspec-file-nul instead): paths are separated with NUL character
    --stdin               DEPRECATED (use --pathspec-from-file=- instead): read paths from <stdin>


C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git reset --hard HEAD~1
HEAD is now at dad3773 prepare for merge and rebase

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git switch -b git-rebase
error: unknown switch `b'
usage: git switch [<options>] [<branch>]

    -c, --create <branch>
                          create and switch to a new branch
    -C, --force-create <branch>
                          create/reset and switch to a branch
    --guess               second guess 'git switch <no-such-branch>'
    --discard-changes     throw away local modifications
    -q, --quiet           suppress progress reporting
    --recurse-submodules[=<checkout>]
                          control recursive updating of submodules
    --progress            force progress reporting
    -m, --merge           perform a 3-way merge with the new branch
    --conflict <style>    conflict style (merge or diff3)
    -d, --detach          detach HEAD at named commit
    -t, --track           set upstream info for new branch
    -f, --force           force checkout (throw away local modifications)
    --orphan <new-branch>
                          new unparented branch
    --overwrite-ignore    update ignored files (default)
    --ignore-other-worktrees
                          do not check if another worktree is holding the given ref


C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git checkout -b git-rebase
Switched to a new branch 'git-rebase'

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepade rebase.sh
"notepade" не является внутренней или внешней
командой, исполняемой программой или пакетным файлом.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git add rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git commit -m "git-rebase 1"
[git-rebase 9ab3490] git-rebase 1
 1 file changed, 5 insertions(+), 3 deletions(-)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push origin git-rebse
error: src refspec git-rebse does not match any
error: failed to push some refs to 'https://github.com/vitsinv/devops-netology/'

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push origin git-rebase
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 456 bytes | 456.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'git-rebase' on GitHub by visiting:
remote:      https://github.com/vitsinv/devops-netology/pull/new/git-rebase
remote:
To https://github.com/vitsinv/devops-netology/
 * [new branch]      git-rebase -> git-rebase

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git add rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git commit -m "git-rebase 2"
[git-rebase 446e51e] git-rebase 2
 1 file changed, 1 insertion(+), 1 deletion(-)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push origin git-rebase
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 378 bytes | 378.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/vitsinv/devops-netology/
   9ab3490..446e51e  git-rebase -> git-rebase

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git merge git-merge
Merge made by the 'recursive' strategy.
 branching/merge.sh | 5 +++--
 1 file changed, 3 insertions(+), 2 deletions(-)

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push
fatal: The current branch git-rebase has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin git-rebase


C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push --set-upstream origin git-rebase
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 377 bytes | 377.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/vitsinv/devops-netology/
   446e51e..452a439  git-rebase -> git-rebase
Branch 'git-rebase' set up to track remote branch 'git-rebase' from 'origin'.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git log --oneline
452a439 (HEAD -> git-rebase, origin/git-rebase) Merge branch 'git-merge' into git-rebase
446e51e git-rebase 2
9ab3490 git-rebase 1
fc70f70 (origin/git-merge, git-merge) merge: use shift
2ad18d0 merge: @ instead *
dad3773 prepare for merge and rebase
16ca229 (tag: v0.1, tag: v0.0, gitlab/main, bitbucket/main) before push
5491f27 help for git & git add
b438fb1 Moved and deleted
d47c68a prepare to delete and move
5edc0c6 Added gitignore
b561454 first commit
511b14d Initial commit

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git reset --hard 446e51e
HEAD is now at 446e51e git-rebase 2

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git log --graph --all
*   commit 452a4390706638b741d2d667301b4869f4810aaf (origin/git-rebase)
|\  Merge: 446e51e fc70f70
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Mon Jul 19 20:18:14 2021 +0300
| |
| |     Merge branch 'git-merge' into git-rebase
| |
| * commit fc70f700cead97ac159e05d4c62c98bb8335a83c (origin/git-merge, git-merge)
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Mon Jul 19 20:01:21 2021 +0300
| |
| |     merge: use shift
| |
| * commit 2ad18d0c068c0d31275fc5c6f6eb76c5bfc60db7
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Mon Jul 19 19:55:46 2021 +0300
| |
| |     merge: @ instead *
| |
* | commit 446e51e19b16be491913a72dc31672de4c2b792e (HEAD -> git-rebase)
| | Author: Viktor Vinogradov <v.vitsin@gmail.com>
| | Date:   Mon Jul 19 20:17:00 2021 +0300
| |
| |     git-rebase 2
| |
* | commit 9ab349030ff207bd33923c35a3d2cd6ebb15f935
|/  Author: Viktor Vinogradov <v.vitsin@gmail.com>
|   Date:   Mon Jul 19 20:15:25 2021 +0300
|
|       git-rebase 1
|
| * commit b42d05e90e2be9799606ac72c025f358ccd929ff (origin/main, origin/HEAD, main)
|/  Author: Viktor Vinogradov <v.vitsin@gmail.com>
|   Date:   Mon Jul 19 20:03:05 2021 +0300
|
|       change rebase.sh
|
* commit dad37735803fcc458d7eb55c23716734371c66e3
| Author: Viktor Vinogradov <v.vitsin@gmail.com>
| Date:   Mon Jul 19 19:51:17 2021 +0300
pick 9ab3490 git-rebase 1
pick 446e51e git-rebase 2

# Rebase 8747635..446e51e onto 8747635 (2 commands)
#
# Commands:
# p, pick <commit> = use commit
# r, reword <commit> = use commit, but edit the commit message
# e, edit <commit> = use commit, but stop for amending
# s, squash <commit> = use commit, but meld into previous commit
# f, fixup [-C | -c] <commit> = like "squash" but keep only the previous
#                    commit's log message, unless -C is used, in which case
#                    keep only this commit's message; -c is same as -C but
#                    opens the editor
# x, exec <command> = run command (the rest of the line) using shell
# b, break = stop here (continue rebase later with 'git rebase --continue')
# d, drop <commit> = remove commit
# l, label <label> = label current HEAD with a name
# t, reset <label> = reset HEAD to a label
# m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
# .       create a merge commit using the original merge commit's
# .       message (or the oneline, if no original merge commit was
# .       specified); use -c <commit> to reword the commit message
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                C:/Users/vitsin/Documents/git/test_git/devops-netology/.git/rebase-merge/git-rebase-todo [unix] (20:32 19/07/2021)                                                                                        1,1 All













git-rebase 1

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# interactive rebase in progress; onto 8747635
# Last command done (1 command done):
#    pick 9ab3490 git-rebase 1
# Next command to do (1 remaining command):
#    pick 446e51e git-rebase 2
# You are currently rebasing branch 'git-rebase' on '8747635'.
#
# Changes to be committed:
#       modified:   branching/rebase.sh
#
# Untracked files:
#       .idea/
#
~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                C:/Users/vitsin/Documents/git/test_git/devops-netology/.git/COMMIT_EDITMSG [unix] (20:35 19/07/2021)                                                                                                      1,1 All















git-rebase 2

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# interactive rebase in progress; onto 8747635
# Last commands done (2 commands done):
#    pick 9ab3490 git-rebase 1
#    pick 446e51e git-rebase 2
# No commands remaining.
# You are currently rebasing branch 'git-rebase' on '8747635'.
#
# Changes to be committed:
#       modified:   branching/rebase.sh
#
# Untracked files:
#       .idea/
#
~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                ~                                                                                                                                                                                                                C:/Users/vitsin/Documents/git/test_git/devops-netology/.git/COMMIT_EDITMSG [unix] (20:36 19/07/2021)                                                                                                      1,1 All


















































[detached HEAD ed14308] git-rebase 2
 1 file changed, 4 deletions(-)
Successfully rebased and updated refs/heads/git-rebase.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>notepad rebase.sh

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git push -u origin git-rebase -f
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 670 bytes | 335.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/vitsinv/devops-netology/
 + 446e51e...ed14308 git-rebase -> git-rebase (forced update)
Branch 'git-rebase' set up to track remote branch 'git-rebase' from 'origin'.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

C:\Users\vitsin\Documents\git\test_git\devops-netology\branching>git merge git-rebase
Updating 8747635..ed14308
Fast-forward