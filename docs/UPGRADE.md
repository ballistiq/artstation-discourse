## Syncing ArtStation discourse with upstream

### Setup

Before you can sync, you need to add a remote that points to the original discourse repository. Needs to be done only once.


```bash
$ git remote add upstream git@github.com:discourse/discourse.git
# Set a new remote

$ git remote -v
# Verify new remote
origin  git@github.com:ballistiq/artstation-discourse.git (fetch)
origin  git@github.com:ballistiq/artstation-discourse.git (push)
upstream  git@github.com:discourse/discourse.git (fetch)
upstream  git@github.com:discourse/discourse.git (push)
```

### Syncing

Fetch upstream and pick latest tag
```bash
$ git fetch upstream
# ...
* [new tag]         v0.9.9.4   -> v0.9.9.4
```

Then merge it into current master
```bash
$ git checkout master
# ensure that you are in master
$ git merge v0.9.9.4
```
