# Submitting a Slurm Job with a non-Bash shell

Slurm (`sbatch`) has problems with `zsh`, at least on Hera. If you are using `zsh` or another non-bash shell, follow the steps below to submit jobs to Slurm.

### 0. make sure your default user shell is `bash`
if you have used `chsh`, you'll need to either explicitly run `sbatch` with Bash or use something similar to the code in Step 2 except for with `/bin/bash` instead of `/bin/zsh` 

### 1. make sure that you don't have any `zsh` or `exec zsh` in `~/.bashrc`, `~/.profile`, or `~/.bash_profile`
we'll add `exec zsh` in the next step

### 2. add the following code to the end of `~/.bash_profile`
```bash
if [[ $- == *i* ]]; then
    if [ -z ${SLURM_SUBMIT_DIR+x} ]; then
        export PATH
        export SHELL=/bin/zsh
        exec /bin/zsh -l
    fi
fi
```
this will run `zsh` if and only if the current shell is 1) interactive and 2) not a Slurm session (the sub session that runs when submitting a Slurm job)
