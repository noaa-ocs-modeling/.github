## Installing Windows Subsystem for Linux

Windows Subsystem for Linux (WSL) is a platform onto which a Linux distribution, such as Ubuntu, can be installed. It provides a Linux shell within Windows that contains a functional Linux kernel, and thus can compile and run programs meant for Linux within that environment.

### 1. Enable `Windows Subsystem for Linux` in Windows Features

Search `Features` in the Windows Start menu, and click on `Turn Windows features on or off` (alternatively, this can be found in `Programs and Features` of the Control Panel). 

**This is the only step that requires administrator privileges.**

<img src="https://user-images.githubusercontent.com/52422935/89196253-f1a26e00-d577-11ea-962f-c145c724e36d.png" width=75%>

Scroll down to `Windows Subsystem for Linux` and check it, then click `OK`

<img src="https://user-images.githubusercontent.com/52422935/89196321-0da60f80-d578-11ea-83e7-c102eaf9c836.png" width=50%>

Reboot when prompted.

### 2. Install your choice of Linux distribution onto WSL

The easiest way to install a Linux distribution onto WSL is through the Microsoft Store.

[<img src='https://developer.microsoft.com/store/badges/images/English_get-it-from-MS.png' alt='Ubuntu WSL' width=20%/>](http://www.microsoft.com/store/apps/9nblggh4msv6?cid=storebadge&ocid=badge)

If you do **not** have access to the Microsoft Store, download [the latest Ubuntu distribution from Microsoft's WSL distribution page](https://docs.microsoft.com/en-us/windows/wsl/install-manual) and run the following command in PowerShell:
```powershell
Add-AppxPackage ~\Downloads\Ubuntu_2004.2020.424.0_x64.appx
```

Now, type `Ubuntu` into the Start Menu and run it:

<img src="https://user-images.githubusercontent.com/52422935/89198259-f6b4ec80-d57a-11ea-84e7-bea3564af709.png" width=75%>

Installation will take a few minutes, after which it will prompt you for a username and password. You now have a Linux shell in Windows.

<img src="https://user-images.githubusercontent.com/52422935/89199012-f9fca800-d57b-11ea-8390-ea38b90c1036.png" width=100%>

You have access to many Windows utilities fron WSL, and many WSL utilties from the Windows shell. [Click here to read more about interoperability between Windows and WSL.](https://docs.microsoft.com/en-us/windows/wsl/interop)
