# Git


# Remove local branches not existing on remote

```sh
git fetch -a -p && git branch -r | awk '{print $1}' | egrep -v -f /dev/fd/0 <(git branch -vv | grep origin) | awk '{print $1}' | xargs git branch -d

```
