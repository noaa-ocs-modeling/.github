# Hera
Hera is run by NOAA.

**User Guide: https://heradocs.rdhpcs.noaa.gov/wiki/index.php/Main_Page**

## Connecting to Hera:
https://rdhpcs-common-docs.rdhpcs.noaa.gov/wiki/index.php/Logging_in

### 1. request access to Hera
https://aim.rdhpcs.noaa.gov/cgi-bin/request.pl

### 2. set up your RSA token
https://rdhpcs-common-docs.rdhpcs.noaa.gov/wiki/index.php/RSA_Login
this can be a physical hardware token or a software token (RSA SecurID Software Token phone app)

### 3. connect to Hera via SSH
```bash
ssh User.Name@hera-rsa.princeton.rdhpcs.noaa.gov
```
OR
```bash
ssh User.Name@hera-rsa.boulder.rdhpcs.noaa.gov
```
when prompted for a password for the first time logging in (if you have not yet set up a PIN), enter the 8-digit RSA token code currently displayed on your RSA token. The system will then prompt you to enter a PIN; this will prepend your token code from now on when logging in (if your pin is `55555555`, and your token code is `12345678`, your password is `5555555512345678`).

### 4. take note of your assigned local port
this will show every time you log in

<img src="https://rdhpcs-common-docs.rdhpcs.noaa.gov/images/rdhpcs-common-docs/Pt_linux_localport.png" width=50%>
<img src="https://user-images.githubusercontent.com/52422935/107557578-cdb78900-6ba7-11eb-82c5-395dec7f3227.png" width=50%>

## SSH Tunnel
### [OPTION A] run SSH with the `-L` option
use your assigned local port ([see above](https://gist.github.com/zacharyburnettNOAA/671d2fe3a51849d2c769c0fe44d19e2c#4-take-note-of-your-assigned-local-port))
```bash
ssh -L <local_port>:localhost:<local_port> User.Name@hera-rsa.princeton.rdhpcs.noaa.gov
```
### [OPTION B] use Putty to create a tunnel
#### 1. create a new Putty configuration
<img src="https://user-images.githubusercontent.com/52422935/107572944-e8dfc400-6bba-11eb-9f95-c149d6c95652.png" width=50%>

#### 2. add a new port to the SSH Tunnel settings page
go to `Connection` -> `SSH` -> `Tunnel` and enter your assigned local port number
<img src="https://user-images.githubusercontent.com/52422935/107572968-f137ff00-6bba-11eb-80c7-a6a76dd2be57.png" width=50%>

then click `Add`

<img src="https://user-images.githubusercontent.com/52422935/107573037-fe54ee00-6bba-11eb-94e0-cdc06d82a46c.png" width=50%>

#### 3. save the session
<img src="https://user-images.githubusercontent.com/52422935/107573068-0876ec80-6bbb-11eb-93a1-381b046b8414.png" width=50%>

## Desktop GUI with X2Go
### 1. download and install X2Go
https://wiki.x2go.org/doku.php/doc:installation:x2goclient

### 2. start an SSH tunnel to Hera ([see above](https://gist.github.com/zacharyburnettNOAA/671d2fe3a51849d2c769c0fe44d19e2c#ssh-tunnel))

### 3. start X2Go and click `Session` -> `New Session`
<img src="https://user-images.githubusercontent.com/52422935/102219080-f3c4f380-3eac-11eb-84f1-694358cf6d68.png" width=75%>
fill in your information as so:

<img src="https://user-images.githubusercontent.com/52422935/102218891-b3fe0c00-3eac-11eb-9df8-e97ed3502bd7.png" width=50%>
then click OK

### 4. double click on your new Session to connect
<img src="https://user-images.githubusercontent.com/52422935/102219134-0c350e00-3ead-11eb-8432-106be55ffebc.png" width=75%>
