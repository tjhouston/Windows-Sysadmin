# Windows-Sysadmin
Tools and tips for managing a windows environment

# Tools #
## PS Exec ## 
PS Exec is a tool that allows you to execute proccesses on other systems. It is also clientless so it works great when you need to work on machines across the network. 
 ### Link to download: ### 
 https://docs.microsoft.com/en-us/sysinternals/downloads/psexec
 
## Enable RDP on Remote Machine on the Domain ##
### Set Registry Value ##
psexec.exe \\<computer name> reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f

### Firewall Change To Allow RDP Traffic ###
psexec.exe \\<computer name> netsh firewall set service RemoteDesktop enable
