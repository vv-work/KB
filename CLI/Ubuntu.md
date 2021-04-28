# Ubuntu

## Installation on Windows

```ps
#Enable 
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
#Download
Invoke-WebRequest -Uri https://wsldownload.azureedge.net/Ubuntu_2004.2020.424.0_x64.appx -OutFile Ubuntu.appx -UseBasicParsing
#Install
Add-AppxPackage .\app_name.appx
```

## Connect

```powershell
ssh coman@home-server
```

## mounting a drive

```bash

sudo lsblk

sudo mount -t ntfs-3g /dev/sdb1 /home/coman/lib
```

bla-bla.
