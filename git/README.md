# Git book

## Facts
Creator: Linus Torvalds(2005)  
Type: DVCS  
Based on: Bitkeeper & Monotone  
Features:  

* Speed
* Non-linear & distributed dev
* Large projects

## Resources
* [Site](http://www.git-scm.com/)
* [Reference](http://www.git-scm.com/docs)
* [Pro Git Book](http://git-scm.com/book/en/v2)
* [GH cheatsheet](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)
* [Atlassian tutorials](https://www.atlassian.com/git/tutorials/)

### Workflows
* [Distribued workflows](http://git-scm.com/book/en/v2/Distributed-Git-Distributed-Workflows#_distributed_git)
* [Feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow)
* [Branching model](http://nvie.com/posts/a-successful-git-branching-model/) (master/development/feature branches/hotfix/release branches)


## Fundamentals
* Snapshots, not differences
* Almost all operations are local
* Integrity via sha-1(40char-str hexa)
* 3 stages : working dir, staging(index), .git dir


## Essential command line

### Config

#### Paths

|Path          |Type  |
|:------------:|:----:|
|/etc/gitconfig|Global|
|~/.gitconfig  |User  |
|.git/config   |Repo  |

### First time setup

#### View currentSettings
```
git config --list
```

#### Identity
```
git config --global user.name "gitname"
git config --global user.email "gitname@users.noreply.github.com"
git config --global core.editor nano
git config --global color.ui auto
git config --global merge.tool diffmerge
```

### Create repositories

#### Init
```
git init
```

#### Clone
```
git clone https://github.com/rkheik/blackbooks.git
git clone https://github.com/rkheik/blackbooks.git dest_dir
```
##### shallow clone(useful on very large repos)
```
git clone --depth depth remote-url
```

### Snapshotting

#### add
```
git add .         # All
git add <file>
git add *.c
```

#### status
```
git status
git status -s      #short
```

#### diff
```
git diff            #changes not stagged
git diff --staged   #staged / last commit; or --cached
git diff file
```

#### commit
```
git commit                         #open default editor
git commit -m "commit message"
git commit -a -m "commit message"  #skip stage area, adding mod files
```

#### reset
unstage

```
git reset HEAD file
```

discard modified file

```
git checkout -- file
```

#### rm
remove
```
rm file
git rm file
```

remove from staging but keep

```
git rm --cached file
```

#### mv

```
git mv README.md README
```

same as

```
mv README.md README
git rm README.md
git add README.md
```


### Branching and Merging

#### branch
view branches
```
git branch
```
last commit on each branch
```
git branch -v
```
create branch
```
git branch testing
```

branch create and switch
```
git checkout -b testing
```

delete no longer needed branch
```
git branch -d testing
```
see branched in current
```
git branch --merged
```


#### checkout
branch switch
```
git checkout testing
```

#### merge
merge to master
```
git checkout master
git merge testing
```

merge changes from master on to feature branch
```
git merge master
```

merge feature, forcing always merge commit(no fast forward)
useful with branch per feature workflow(preserving branch topology)
```
git checkout dev
git merge --no-ff feature
```

#### mergetool
useful on merge conflicts
```
git mergetool
git commit     #finish merge
```

#### log
log decorate branches and graph
```
git log --oneline --decorate --graph --all
```

#### stash

list
```
git stash list
```

temporarilly stores all modified tracked files and staged
```
git stash
```

restores stash changes
```
git stash pop
```

discard most recent stashed
```
git stash drop
```

#### tag
listing
```
git tag
```

list w/search pattern
```
git tag -l 'v1.*'
```

annotated
```
git tag -a v1.0 -m 'version 1.0'
```

lightweight
```
git tag v0.9   #no additional info
```

tag specific commit
```
git tag -a v1.1 [commit hash]
```

push tags
```
git push origin v1.1
```

push all tags
```
git push origin --tags
```

checking out tags
```
#git checkout -b [branchname] [tagname]
git checkout -b branch-v1.0 v1.0
```
#### rebase
**Do not rebase commits that exist outside your repository.**

**TODO**
http://think-like-a-git.net/sections/rebase-from-the-ground-up.html

### Sharing and updating projects

#### fetch
```
git fetch
#git fetch [remote-name]
git fetch origin
```

#### pull
```
git pull
```
**TODO**

#### push
```
#git push [remote-name] [branch-name]
git push origin master
```

#### remote
show
```
git remote
git remote -v  #show url
```

add remote
```
git remote add other [url]
```

inspecting a remote
```
git remote show origin
```

removing and renaming remotes
```
git remote rename other other2
git remote rm other
```


#### submodule
add repo as submodule
```
git submodule add [url]
```

clone repo with submodules
```
git clone [url] submodule_dir
cd submodule_dir
git submodule init
git submodule update
```

git submodule update one line
```
git clone --recursive [url]
```


### Inspection

#### show
```
git show <object>
git show v1.0     #tag
git show fb6599e  #commit
```

#### log
```
git log
git log --pretty=oneline
# reference names
git log --oneline --decorate
#h short hash, an author name, ar author date, s subject
git log --pretty=format:"%h -%an, %ar :%s"
#branch/merge ascii representation
git log --pretty=format:"%h :s" --graph
git log --since=2.weeks
#last n commits
git log --author=rkheik
#git log -n
git log -1
# git log decorate branches and graph
git log --oneline --decorate --graph --all

```


### Misc

#### Verison
```
git --version
```

#### .gitignore
Resource
[gitignore for different langs](https://github.com/github/gitignore)
```text
# no .a files
*.a
#ignore TODO
/TODO
#ignore files in build dir
build/
#ignore pdfs in doc/*.pdf doc/random/*.pdf
doc/**/*.pdf
```

#### Aliases
```
git config --global alias.unstage 'reset HEAD --'
git unstage file
```

#### Archive
```
git archive --format zip --output /path/file.zip master 
```
#### Handle big repos
[big repos tips](http://blogs.atlassian.com/2014/05/handle-big-repositories-git/)
