# Active Directory Lateral Movement

- Windows Services
- WinRM
- PsExec
- RDP
- WMI
- DCOM
- Webclient
- CrackMapExec
- MSSQL


## Windows Services



## PowerShell Remoting
#Enable PowerShell Remoting on current Machine (Needs Admin Access)

''' Enable-PSRemoting '''

#Entering or Starting a new PSSession (Needs Admin Access)
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>