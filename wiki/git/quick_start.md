# Getting Started
### 0. install Git from https://git-scm.com/download:
On Windows, this will install a Git Bash command-line interface, which you can access from the right-click menu or Start Menu. There are also several GUI clients for Git, such as [GitHub Desktop](https://desktop.github.com/) and [Atlassian SourceTree](https://www.sourcetreeapp.com/), but this guide will use command-line commands.

### 1. **clone** a repository to your local workspace:
you can specify your desired local directory
```bash
git clone https://github.com/noaa-ocs-modeling/nemspy /path/to/local/directory/nemspy
cd /path/to/local/directory/nemspy
```
by default, the repository will start on the **master** branch

### 2. **checkout** the branch you want to work on:
Usually, the default (**main**) branch is protected from working directly on it (since it acts as the user-facing code that should always be stable). I you wish to make a change, you will want to switch to (**checkout**) a different branch.

You can see a list of branches by doing
```bash
git branch -a
```

Try switching to the **develop** branch: 
```bash
git checkout develop
```

You can also make a new branch (for instance if you want a personal space to work on things without messing anything up in the actual code):
```bash
git checkout -b new_branch_name
```

### 3. **pull** any changes that have been made on the remote server to bring your local files up-to-date
If you just cloned this repository, it should be up to date already. However, it is good to get into the practice of pulling frequently, just to make sure you 
```bash
git pull
```

### 3. make changes using your editor or IDE of choice
Many IDEs, such as PyCharm, Atom, Sublime Text, etc, have a Git interface built-in that will let you see, commit, and push changes.

If you don't use an IDE with these features, or if you prefer the command line, you can always use `git status` to check your changes.
```bash
git status
```

### 4. **commit** your changes with a descriptive message:
Now it's time to package up your changes into a **commit**. This commit will be the thing that you push to GitHub / GitLab / etc. 
Add any new files that should be tracked:
```bash
git add new_file.txt another_file.m directory_to_add/*
```
and commit those files as so:
```bash
git commit -m "Here is a description of what I changed"
```
It's important to understand here that *you have not pushed anything yet*. This commit (and any more commits you make) will not travel to the remote server until you do a **git push**.

### 5. **push** your own changes to the remote:
```
git push
```
Once you push your changes, they will be applied *only on the current branch*. In order for these changes to be applied in a different branch (say in **master**), you will have to **merge** the branches together. This is ususally best done on the remote side (**pull requests** on GitHub, **merge requests** on GitLab) and can be done through the website of you server.
