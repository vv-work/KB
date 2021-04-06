# PowerShell

## Basics

```powershell
function subtract ($from, $count) { $from - $count } #function
```

## Execution policy

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
Get-ExecutionPolicy -List
```

## Making shortcut

Powershell Shortcut Location
>C:\Users\admin\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Windows PowerShell
```powershell
C:\Windows\SysWOW64\WindowsPowerShell\v1.0\powershell.exe -noexit (. B:\Lib\Proj\PS\Default.ps1)
```
>Path = C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Windows PowerShell


## Install My script

```powershell
. B:\Lib\Proj\PS\Default.ps1
```

## Starting Job
To Start independment instance of *Visual Studio Code*:

```powershell
 start-job {code}
```

## Starting job in current location 

Start-Job { code args[0] } -ArgumentList (gl)

### old way
Start-Job { param([string[]]$path)code $path } -ArgumentList (Get-Location)

### Donload all git respos from list

 foreach($r in $repos){ if($r.Contains("github.com")){git clone $r}}
Cloning into 'Rider-Replica'...