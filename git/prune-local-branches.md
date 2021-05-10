# How to prune local tracking branches that do not exist on remote

```sh
git remote prune origin

git branch -vv | grep ': gone]'|  grep -v "\*" | awk '{ print $1; }' | xargs git branch -D
```
