# What Is Git?
Git is a very easy way for a lot of people to work on the same files at once without conflict and with a detailed history of all changes. It's designed to let multiple developers work on separate features of the same project simultaneously. Git is organized into a hierarchy of **repositories** (individual coding projects) and **branches** (separate versions of the same project).

Here is an example of a Git repository on GitHub: https://github.com/noaa-ocs-modeling/nemspy

The workflow is relatively simple: first, you **clone** the remote repository from a Git server (GitHub, GitLab, etc), which makes a local copy of all the files and version history on your own computer. Then, you make the changes you want to make to your local copy, and wrap up all your changes into a packaged difference file called a **commit**, to which you can attach a message describing what you’ve changed. Once you’ve made one (or several) commits, you can then **push** all the commits to the remote server, which is when your changes travel back to the remote repository and are applied for everyone to see. Git will automatically resolve most conflicts with changes that other people have made in the meantime, even multiple changes to the same file.

Repositories can have different **branches**. Branches are parallel instances of the code, used to keep track of separate issues or features. Each branch is made up of a distinct set of changes from the main files, all related to the specific feature that the branch represents. In Git, you **checkout** a branch to switch your local files to its specific changes. Once these issues or features are implemented, branches can be **merged** back together, folding all the changes made since they were split and combining their files. Common convention when working with Git is to have a **main** branch, the current stable codebase for the users, a **develop** branch, for all the newly developed changes or features that haven’t been fully tested yet, and a multitude of other branches for individual features where all the actual work is done.

common convention:
- **main** <- this is where the most stable code should live; a user should be able to run this branch without any problems
- **develop** <- this is where the upcoming features should be integrated into the code in preparation for making things stable and putting them into the main branch. This branch will inherently be less stable than the main branch.
- **feature/do_cool_thing** <- this is where cutting-edge development should be done on some new feature or change.
