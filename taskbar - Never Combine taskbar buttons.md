# taskbar - Never Combine taskbar buttons

You'll have to use this method until they update it (I wrote this script based on the article.)

Open Powershell -> Start Menu -> Run -> taskmgr -> File -> Run new Task -> %SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe -> Select "Create this task with administrative privileges." -> Click OK.
```powershell
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope LocalMachine -Force
# Restore the Classic Taskbar in Windows 11
New-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Shell\Update\Packages" -Name "UndockingDisabled" -PropertyType DWord -Value "00000001";
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Shell\Update\Packages" -Name "UndockingDisabled" -Value "00000001";
# Disable Taskbar / Cortana Search Box on Windows 11
New-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\Search" -Name "SearchboxTaskbarMode" -PropertyType DWord -Value "00000000";
Set-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\Search" -Name "SearchboxTaskbarMode" -Value "00000000";
# Ungroup Taskbar Icons / Enable Text Labels in Windows 11
New-ItemProperty -Path "HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer" -Name "NoTaskGrouping" -PropertyType DWord -Value "00000001";
Set-ItemProperty -Path "HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer" -Name "NoTaskGrouping" -Value "00000001";
#Restart Explorer to see the changes
./taskkill /f /im explorer.exe;
./CMD /Q /C START /REALTIME explorer.exe;
```
Run this below if you want to reverse the above changes...
```powershell
#Run this to reverse the changes
Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Shell\Update\Packages" -Name "UndockingDisabled" -Value "00000000"
Set-ItemProperty -Path "HKCU:\Software\Microsoft\Windows\CurrentVersion\Search" -Name "SearchboxTaskbarMode" -Value "00000001";
Set-ItemProperty -Path "HKCU:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer" -Name "NoTaskGrouping" -Value "00000000";
#Restart Explorer to see the changes
./taskkill /f /im explorer.exe;
./CMD /Q /C START /REALTIME explorer.exe;
```