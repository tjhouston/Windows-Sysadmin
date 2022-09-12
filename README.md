# Windows-Sysadmin
Tools and tips for managing a windows environment

## Enable RDP on remote machine on the domain ##
### Set Registry Value ##
psexec.exe \\<computer name> reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f

### Make firewall Change ###
psexec.exe \\<computer name> netsh firewall set service RemoteDesktop enable
