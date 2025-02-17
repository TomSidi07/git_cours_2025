# NOTES : GIT

- Git is a version tracking system

- Github and GitLab are providers built on the idea of Git

## Set Git default editor : windows

- vscode : git config --global core.editor "code --wait"
- nano : git config --global core.editor "/usr/bin/nano"

## git config setting

### global : with --global

- list all config :

  `git config list --global`

- set global user:

  `git config --global user.name "_name"`

  `git config --global user.email "_email"`

### setting : for a repo without --global

- set global user:
  `git config user.name "_name"`
  `git config user.email "_email"`

## GIT ADD & GIT COMMIT

### git add : Transit

- command `git add` tells to Git `follow all this file moves 👀`

`git add file.txt` --add it to the--> `stagging area(index area)`

### git commit :

- command `git commit` tells to Git `take a snapshot of the current state of all the files you've been follwed`

`git commit -m "message"`

### workflow:

`working_dir` -- `-gitadd`---> `stagging area`-- `-gitcommit`---> `local repo`

### GIT PUSH & GIT PULL

<!-- GIT PUSH -->

## GIT LOG

- cli :
  git log
  git log -\_index_of_commit
  git log --oneline
  git log --graph

## UNDO COMMIT

### stage area

    git reset <file>
    git restore --staged <file>

### restore last commit (files contents)

#### basic commands

    git restore .
    git restore <file>
    git restore -s HEAD~no <file>
    git checkout HEAD~no - <file> (not optimale)

#### save in a new file

git show HEAD~:<file> > <newfile.ext>

### back to a target commit

    git reset --hard <commits_hash>

### undo a commit

  - git revert HEAD~no 
    (create a new commit to mark the revertion of commits)

  - git revert -n(--no-commity) HEAD~4..HEAD

    or

  - git reset --hard (change the commit history)
