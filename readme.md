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
