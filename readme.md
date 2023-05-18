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

## Bundle 2

### Exercise 1

```bash
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add service.html
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "Add Service Page"
[ft/bundle-2 2e102f0] Add Service Page
 1 file changed, 12 insertions(+)
 create mode 100644 service.html
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$  git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 495 bytes | 495.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Derick1530/git-exercises/pull/new/ft/bundle-2
remote:
To github.com:Derick1530/git-exercises.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
Branch 'ft/bundle-2' set up to track remote branch 'ft/bundle-2' from 'origin'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$
```

### Exercise 2

```bash

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout main
Switched to branch 'main'
razac@Razac:~/Documents/GitHub/Ojemba/razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 628 bytes | 628.00 KiB/s, done.
From github.com:Derick1530/git-exercises
   b320937..5180825  main       -> origin/main
Updating b320937..5180825
Fast-forward
 about.html   |  12 ++
 home.html    |  12 ++
 readme.md    | 259 +++++++++++++++++++++++++++++++++++++++++
 service.html |  12 ++
 4 files changed, 295 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html
 razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git merge main
Updating b320937..5180825
Fast-forward
 about.html   |  12 ++
 home.html    |  12 ++
 readme.md    | 259 +++++++++++++++++++++++++++++++++++++++++
 service.html |  12 ++
 4 files changed, 295 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 service.html


```

## Bundle 3

### Exercise 1

```bash
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout -b ft/team
Switched to a new branch 'ft/team'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* ft/team
  main
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "Create team page"
[ft/team-page 85477ca] Create team page
 1 file changed, 1 insertion(+), 1 deletion(-)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push --set-upstream origin ft/team-page
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 303 bytes | 303.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Derick1530/git-exercises/pull/new/ft/team-page
remote:
To github.com:Derick1530/git-exercises.git
 * [new branch]      ft/team-page -> ft/team-page
Branch 'ft/team-page' set up to track remote branch 'ft/team-page' from 'origin'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git log
commit 85477cae2367538c93c6645ecf60044945931ebe (HEAD -> ft/team-page, origin/ft/team-page)
Author: Derick1530 <DerickZIHALIRWA07@gmail.com>
Date:   Thu May 18 06:34:25 2023 +0300

    Create team page

commit 555c7553d22de41491
8588b98e910e28be43d552 (o
rigin/ft/service-redesign
, ft/service-redesign)
Author: Derick1530 <Deric
kZIHALIRWA07@gmail.com>
Date:   Thu May 18 06:30:
24 2023 +0300

    Add terminal command

commit 94b74b5e7014361f23
aa637201e4b6682af66f50
Merge: f5954db e710b1f
Author: Derick1530 <Deric
kZIHALIRWA07@gmail.com>
Date:   Thu May 18 06:26:
11 2023 +0300

    Resolved Conflict

commit e710b1f99e02f8f3e1
1bc62b47937bf8802ae3b7 (o
rigin/main, main, ft/team
, ft/contact-page)
Author: Derick1530 <Deric
kZIHALIRWA07@gmail.com>
Date:   Thu May 18 06:15:
41 2023 +0300

    Change title

commit f5954dbe3e04172137
6a16f45fd91486bec79bf1
Author: Derick1530 <Deric
kZIHALIRWA07@gmail.com>
Date:   Thu May 18 06:13:
46 2023 +0300

    New commit

commit 5180825391a87d5281
c9404a8fcdb42089d0a434
Merge: b320937 a454a4d
Author: Derick1530 <Deric
kZIHALIRWA07@gmail.com>
Date:   Thu May 18 06:08:
37 2023 +0300

    Merge pull request #2
 from Derick1530/ft/bundl
e-2
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/team
ft/team
ft/team-page
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/team-page
Already on 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "Add a line"
[ft/team-page 876b3e4] Add a line
 1 file changed, 1 insertion(+)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
Enumerating objects: 5, done.
Counting objects:  20% (1Counting objects:  40% (2Counting objects:  60% (3Counting objects:  80% (4Counting objects: 100% (5Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects:  33%Compressing objects:  66%Compressing objects: 100%Compressing objects: 100% (3/3), done.
Writing objects:  33% (1/Writing objects:  66% (2/Writing objects: 100% (3/Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas:remote: Resolving deltas:remote: Resolving deltas:remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:Derick1530/git-exercises.git
   85477ca..876b3e4  ft/team-page -> ft/team-page
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "Add Faq Page"
[ft/faq-page 1e8e17c] Add Faq Page
 1 file changed, 12 insertions(+)
 create mode 100644 faq.html
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git pus
git: 'pus' is not a git command. See 'git --help'.

The most similar commands are
        push
        pull
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push --set-upstream origin ft/faq-pagects: 4, done.
Counting objects:  25% (1Counting objects:  50% (2Counting objects:  75% (3Counting objects: 100% (4Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects:  33%Compressing objects:  66%Compressing objects: 100%Compressing objects: 100% (3/3), done.
Writing objects:  33% (1/Writing objects:  66% (2/Writing objects: 100% (3/Writing objects: 100% (3/3), 494 bytes | 494.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas:remote: Resolving deltas:remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Derick1530/git-exercises/pull/new/ft/faq-page
remote:
To github.com:Derick1530/git-exercises.git
 * [new branch]      ft/faq-page -> ft/faq-page
Branch 'ft/faq-page' set up to track remote branch 'ft/faq-page' from 'origin'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git revert 876b3e4f686b52ad9addbfb51047e3b73900ded8
[ft/team-page d64f75e] Revert "Add a line"
 1 file changed, 1 deletion(-)
```

### Exercise 2

```bash
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/faq-page
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "Change Title"
[main 306ab25] Change Title
 1 file changed, 1 insertion(+), 1 deletion(-)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 310 bytes | 310.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
giTo github.com:Derick1530/git-exercises.git
   fb9dc76..306ab25  main -> main
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git add .
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git commit -m "Change title"
[ft/home-page-redesign 1e04e46] Change title
 1 file changed, 1 insertion(+), 1 deletion(-)
razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

razac@Razac:~/Documents/GitHub/Ojemba/ojemba-project/github-exercice$  git push --set-upstream origin ft/home-page-redesign
```
