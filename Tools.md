# PowrShell


## Basics
Creating arrays


## SSH
[Tutorial that worked](https://www.tutorialdocs.com/article/windows-openssh-tutorial.html)

## Make powershlel default

```powershell
New-ItemProperty -Path "HKLM:\SOFTWARE\OpenSSH" -Name DefaultShell -Value "C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe" -PropertyType String -Force
```

```Powershell
ssh coman@104.42.35.28
ssh-keygen -y -f ~/.ssh/id_rsa > ~/.ssh/id_rsa.pub

cat ~/.ssh/id_rsa.pub #see your pubic key

```
## Add tool
```powershell
[System.Environment]::SetEnvironmentVariable('PATH',$Env:PATH+';c:\program files\7-zip')
#for that seession

[System.Environment]::SetEnvironmentVariable('PATH',$Env:PATH+';B:\Programs\Microsoft VS Code\',[System.EnvironmentVariableTarget]::Machine)
#save to the machine
```
## WebRequests

```powershell
    Invoke-WebRequest -Uri "https://ftp.nluug.nl/pub/vim/pc/gvim82.exe" -UseBasicParsing
    Invoke-WebRequest -Uri "https://ftp.nluug.nl/pub/vim/pc/gvim82.exe" -OutFile gvim82.exe
    
```
## install Vim
```powershell
Iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex
choco install vim

$env:PROGRAMDATA\ssh\sshd_config 

Set-ExecutionPolicy Bypass
Iwr https://chocolatey.org/install.ps1 -UseBasicParsing | iex
choco install nano -y
```


## Archives
~~Expend~~-7Zip
Compress-7Zip

## Shortcuts
```PoserShell

    cmd /c mklink B:\Lib\Top\MD.lnk B:\Lib\Books\Syntaxis\MD.pdf

    cmd /c mklink /d B:\Lib\Top\Books.lnk B:\Lib\Books
```



# Git
## Removign large file from history
>git filter-branch --force --index-filter  'git rm --cached --ignore-unmatch path/to/ceo.jpg'  --prune-empty --tag-name-filter cat -- --all

## Visual Studio
(IHA)Intel Hardware Accelaration  for Android emulator


## Shared tools location
C:\Program Files (x86)\Microsoft Visual Studio\Shared



# Azure

>Working with resources
```powershell
$vmData = az vm show --name BuildStation --resource-group BuildStation_group | ConvertFrom-Json 
$ip.virtualMachine.network.publicIpAddresses.ipAddress
```