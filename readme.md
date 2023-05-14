# Git exercises

## Bundle 1

### Exercise 1

```bash
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git init
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/razac/Documents/GitHub/Ojemba/ojemba-project/github-exercice/.git/
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git branch -M main
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git status
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        readme.md

nothing added to commit but untracked files present (use "git add" to track)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add readme.md
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   readme.md

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "First Init"
[main (root-commit) b320937] First Init
 1 file changed, 5 insertions(+)
 create mode 100644 readme.md
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git remote add origin git@github.com:Derick1530/git-exercises.git
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
fatal: The current branch main has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin main

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 259 bytes | 259.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To github.com:Derick1530/git-exercises.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout -b dev
Switched to a new branch 'dev'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout -b test
Switched to a new branch 'test'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout dev
Switched to branch 'dev'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git branch -D test
Deleted branch test (was b320937).
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git status
On branch dev
nothing to commit, working tree clean
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push --set-upstream origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Derick1530/git-exercises/pull/new/dev
remote:
To github.com:Derick1530/git-exercises.git
 * [new branch]      dev -> dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$

```

### Exercise 2

```bash
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash
Saved working directory and index state WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash list
stash@{0}: WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git branch
* dev
  main
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash
Saved working directory and index state WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash list
stash@{0}: WIP on dev: b320937 First Init
stash@{1}: WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add team.html
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash
Saved working directory and index state WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash list
stash@{0}: WIP on dev: b320937 First Init
stash@{1}: WIP on dev: b320937 First Init
stash@{2}: WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash
Saved working directory and index state WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (42c6ee4bd78c46423939527a6b53ee50a794be95)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash
Saved working directory and index state WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git list
git: 'list' is not a git command. See 'git --help'.

The most similar commands are
        bisect
        rev-list
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash list
stash@{0}: WIP on dev: b320937 First Init
stash@{1}: WIP on dev: b320937 First Init
stash@{2}: WIP on dev: b320937 First Init
stash@{3}: WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ ^C
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{1} (4bd44781c8690839666b5966eb222f8ac34914da)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash
Saved working directory and index state WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash list
stash@{0}: WIP on dev: b320937 First Init
stash@{1}: WIP on dev: b320937 First Init
stash@{2}: WIP on dev: b320937 First Init
stash@{3}: WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ ^C
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash pop stash@{1}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{1} (5e9e0ad2952b81c50265ebba363dadcc40de82de)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash
Saved working directory and index state WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash pop stash@{2}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{2} (43ce39cad634f13c7869aba2f062b63022033110)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash list
stash@{0}: WIP on dev: b320937 First Init
stash@{1}: WIP on dev: b320937 First Init
stash@{2}: WIP on dev: b320937 First Init
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash pop stash@{2}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   readme.md

Dropped stash@{2} (d30d9086ddb8de2c8683bcdb3b2aa482407c3507)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "Set up home and about pages"
[dev dd26836] Set up home and about pages
 3 files changed, 107 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 1.65 KiB | 844.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
To github.com:Derick1530/git-exercises.git
   b320937..dd26836  dev -> dev
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git stash pop
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (ae0604a1878da7be42f310bd76ce020a33d9f1b8)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git reset --hard
HEAD is now at dd26836 Set up home and about pages
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ ^C
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$
```
