# Forking a repository

## creating a fork
If you wish to copy or otherwise work on a repository in your own personal space, you can **fork** a repository. On GitHub, this is done by using the `Fork` button on the top right of the repository home page.

## keeping a fork up-to-date with the original (upstream) repository
1. add the original repository (that you forked from) as an additional remote (alongside the default `origin`) from your local files
```bash
git remote add upstream https://github.org/other-user/repository-name
```
You should now be able to see the remote when listing remotes:
```bash
git remote -v
```
```
origin  https://github.org/you/repository-name.git (fetch)
origin  https://github.org/you/repository-name.git (push)
upstream  https://github.org/other-user/repository-name.git (fetch)
upstream  https://github.org/other-user/repository-name.git (push)
```

2. pull from the `upstream` remote into the local master branch
```bash
git pull upstream master
```
3. push the new commits from your upstream (`upstream`) remote to your forked (`origin`) remote
```bash
git push
```

## making a Pull Request to request the original (upstream) repository merge your changes
On your forked repository, click Pull Requests, and make a new one. You should have the option to set the Target branch to be in the upstream repository. Once created, this pull request will appear on the upstream repository's page.
