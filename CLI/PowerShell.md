# PowerShell

## Emoji 
🔥🤔💖t

## Basics

```powershell
function subtract ($from, $count) { $from - $count } #function
```

## Environment 

## Moduels

`D:\Users\admin\Documents\WindowsPowerShell\Modules` - old loction
`B:\myprograms\powershell\7\Modules\` - current location

#Best Way
$env:Path +=";B:\MyPrograms\Git"

#More complex
$Value= $env:Path
[System.Environment]::SetEnvironmentVariable('Path',$Value,[System.EnvironmentVariableTarget]::Process);

[System.Environment]::GetEnvironmentVariable('Path',[System.EnvironmentVariableTarget]::Process);
[System.Environment]::GetEnvironmentVariable('Path',[System.EnvironmentVariableTarget]::Machine);
[System.Environment]::GetEnvironmentVariable('Path',[System.EnvironmentVariableTarget]::User);
```
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
 

## Execution policy

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine
Get-ExecutionPolicy -List
```

## Making shortcut

### IIS manager location 
>%windir%\system32\inetsrv\InetMgr.exe

### Winodws Terminal Location
>D:\Users\admin\AppData\Local\Microsoft\WindowsApps\Microsoft.WindowsTerminal_8wekyb3d8bbwe

### Powershell Shortcut Location
>C:\Users\admin\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Windows PowerShell
```powershell
B:\MyPrograms\PowerShell\7\pwsh -f "B:\Lib\Proj\PS\Default.ps1" -wd "B:\Temp" -noexit
C:\Windows\SysWOW64\WindowsPowerShell\v1.0\powershell.exe -noexit (. B:\Lib\Proj\PS\Default.ps1)
```
>Path = C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Windows PowerShell

### For terminal
```powershell 
B:\MyPrograms\PowerShell\7\pwsh -f "B:\Lib\Proj\PS\Default.ps1" -wd "B:\Temp" -noexit

```
