# Useful Commands:
**Add and commit**:
```
git add . -- name of the file as well, use "." for all added/modified/deleted files
git commit -m "message"
----
git commit -am "message" # acts as a two-in-one using the "am" flag
```
**Alias Commands**
```
git config --global alias.s "status"
# usage -> git s
```
**Alias to see all aliases**
```
git config --global alias.alias "config --get-regexp ^alias\."
# usage -> git alias # shows all aliases
# source -> https://stackoverflow.com/questions/7066325/list-git-aliases
```
**Amend top git message**
```
git commit --amend -m "say this instead"
```
**Amend git commit with new files while keeping message**
```
git add .
git commit --amend --no-edit
```
**Better usage for stash**
```
git stash save nameofstash
git stash list --list out all stashes by index
git stash apply 0 -- apply stash corresponding at index 0
git stash drop 0 -- delete stash corresponding at index 0
```
**See all branches in commandline logs**
```
git log --graph --oneline --decorate
```
**Squash**
```
git rebase main --interactive #do when working on feature branch, not directly on master/main
```

**Cleanup/Destroy all local changes**
```
git fetch origin
git reset --hard origin/master
git clean -df #remove untracked directory/file(s)
```
**Go to previous branch**
```
git checkout -
```
**Set repo origin**
```
git remote add origin [repo-url] #if not set
git remote set-url origin [repo-url] #if already set and updating to new origin
```
# Sources

* [Stackoverflow tip for seeing all alias](https://stackoverflow.com/questions/7066325/list-git-aliases)
* [13 Advanced (but useful) Git Techniques and Shortcuts
](https://www.youtube.com/watch?v=ecK3EnyGD8o&ab_channel=Fireship)
* [Combining Git commits with squash
](https://www.youtube.com/watch?v=V5KrD7CmO4o&ab_channel=TheModernCoder)