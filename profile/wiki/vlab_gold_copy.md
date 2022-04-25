# Gold Copy backup of OCS repositories on VLAB 

To satisfy NOAA's policy to have a "gold copy backup" of source code, 
we have set up a daily backup system on VLAB that downloads the latest commits from GitHub
to a workspace on the VLAB Jenkins server. 

The repository is set up as a series of submodules pointing to public repositories in the GitHub organization:
https://vlab.noaa.gov/redmine/projects/noaa-ocs-modeling/repository/noaa-ocs-modeling

Every day, a Jenkins job starts that runs `git submodule update --remote` on the repository, which goes into each submodule and pulls the latest commits:
https://vlab.noaa.gov/jenkins/job/noaa-ocs-modeling-refresh/ws/

The actual code is stored in the persistent Jenkins workspace.

There shouldn't be any actions required to preserve continuity of this backup; it should run every day automatically.
However, NEW repositories in the GitHub organization will need to be manually added to this repository
in order for them to be backed up on VLAB. You can do this by doing the following:
```shell
git clone https://vlab.noaa.gov/code-review/a/noaa-ocs-modeling
cd noaa-ocs-modeling
git submodule add https://github.com/noaa-ocs-modeling/new_repo_name
git add new_repo_name
git commit -m "added a new submodule that points to new_repo_name"
git push
```
