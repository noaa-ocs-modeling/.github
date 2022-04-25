# Stampede2
Stampede2 is run by the Texas Advanced Computing Center (TACC).

**User Guide: https://portal.tacc.utexas.edu/user-guides/stampede2**

## Connecting to Stampede2:
### 1. create an account with DesignSafe
https://www.designsafe-ci.org/account/register/

### 2. SSH into `stampede2.tacc.utexas.edu`
```bash
ssh username@stampede2.tacc.utexas.edu
```
you may optionally set up SSH key authentication instead of a password

## Desktop GUI with VNC
### 1. create the file **`job.vnc`** in your home directory:
```bash
#SBATCH -J vncserver           # Job name
#SBATCH -o vncserver.out       # Name of stdout output file (%j expands to jobId)
#SBATCH -e vncserver.err       # Name of error output file
#SBATCH -p development         # Queue name
#SBATCH -N 1                   # Total number of nodes requested (68 cores / node)
#SBATCH -n 8                   # Total number of xpi tasks requested
#SBATCH -t 02:00:00            # Run time (hh:mm:ss) - 2 hours for development queues
```
### 2. run the file as a Slurm job:
```bash
sbatch -D ~/ -p normal -t 100 ~/job.vnc -geometry 1920x1020 2>&1
```

### 3. start VNC server
```bash
vncstart
```
note down the port number VNC Server prints out

### 4. connect with a VNC client
connect with the port number given by VNC server when it started; for instance, `stampede2.tacc.utexas.edu:5900`

