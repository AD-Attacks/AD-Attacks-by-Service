---
description: Understand Lateral Movement in Windows
---

# Learn

### Content

[**1. Active Directory Lateral Movement**](lateralmovement.md#heading--1)

* [1.1. Understand Lateral Movement in Windows](lateralmovement.md#heading--1-1)
* [1.2. What can we use to Move laterally?](lateralmovement.md#heading--1-2)

[**2. Move laterally**](lateralmovement.md#heading--2)

* [2.1. Using PowerShell](lateralmovement.md#powershell-remoting)
  * [2.1.1. Not so basic text formatting](lateralmovement.md#heading--2-1-1)
* [2.2. Windows Services](lateralmovement.md#heading--2-2)
* [2.3. Abusing Remote Desktop Protocol - RDP](lateralmovement.md#heading--2-3)

***

## Active Directory Lateral Movement



### What can we use to Move laterally?

* Windows Services
* WinRM
* PsExec
* RDP
* WMI
* DCOM
* Webclient
* CrackMapExec
* MSSQL

### PowerShell Remoting

PowerShell Remoting offers a powerful way for administrators to remotely manage Windows systems, execute commands, and move laterally across a network while maintaining a stealthy profile. It leverages the Windows Remote Management (WinRM) service, which is the Microsoft implementation of the WS-Management Protocol for remote management. PowerShell Remoting is integrated into the Windows operating system, making it a convenient option for administrators and attackers alike.

**Setting Up PowerShell Remoting**

To utilize PowerShell Remoting effectively, it's paramount to ensure that the target system has PowerShell Remoting enabled and properly configured. Here's how to enable it:

```powershell
Enable-PSRemoting -Force
```

This command needs to be executed with administrative privileges. The `-Force` parameter suppresses any user prompts, facilitating automation and scripting.

**Initiating a Remote Session**

With PowerShell Remoting enabled, you can start a remote session using either the computer name or the session object created earlier:

```powershell
Enter-PSSession -ComputerName <Name>
```

or

```powershell
Enter-PSSession -Session $sess
```

These commands allow for interactive management of remote systems. It's worth noting that PowerShell Remoting requires administrative access on the target machine, making it crucial for users to have the necessary permissions.

**Utilizing PowerShell Remoting for Lateral Movement**

PowerShell Remoting can be a subtle tool for lateral movement within a network. By executing remote commands or scripts, an operator can explore the network, gather information, and potentially escalate privileges without directly logging into systems. This can often evade detection from traditional monitoring systems that are not configured to watch for PowerShell Remoting activities.

**Security Considerations**

While PowerShell Remoting is a powerful tool, its misuse by attackers highlights the importance of securing it within an environment. Ensuring that only authorized users have access, monitoring for unusual remoting activities, and using advanced threat detection tools that specialize in identifying PowerShell abuse are all critical measures to protect against unauthorized lateral movement.

By integrating PowerShell Remoting into your lateral movement strategies, with a keen understanding of its capabilities and security implications, you can significantly enhance both the efficiency and stealth of your operations within Windows environments.

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

### Abusing Remote Desktop Protocol - RDP

If we have a NTLM hash we can have an RDP session

#### xFreeRDP

```bash
xfreerdp  +compression +clipboard /dynamic-resolution +toggle-fullscreen /cert-ignore /bpp:8  /u:<Username> /pth:<NTLMHash> /v:<Hostname | IPAddress>
```

```powershell
$sess = New-PSSession -ComputerName <Name>
Enter-PSSession -ComputerName <Name> OR -Sessions <SessionName>
```

#### Mitigation Strategies for RDP Vulnerabilities

To enhance the security posture against abuse of Remote Desktop Protocol (RDP), it's critical to implement strong mitigation strategies. Employing these measures can significantly reduce the risk associated with unauthorized RDP access:

* **Network Level Authentication (NLA)**: Enable NLA on RDP sessions. This requires the connecting user to authenticate before establishing an RDP session, thereby providing an additional layer of security.
* **Complex Passwords and Account Lockout Policies**: Use complex passwords and implement account lockout policies. This makes brute-force attacks more difficult and helps in protecting against unauthorized access attempts.
* **Update and Patch Systems**: Regularly update and patch operating systems and applications. This ensures vulnerabilities are patched, which might otherwise be exploited to gain unauthorized access.
* **Limit RDP Access through Firewalls**: Restrict RDP access on firewalls to specific IP addresses or IP ranges. This minimizes the attack surface by allowing only known and trusted IP addresses to initiate RDP connections.
* **Use VPN for Remote Access**: Require the use of a VPN for remote access. This ensures that RDP connections are made through a secure, encrypted tunnel, further securing the data in transit.
* **Two-Factor Authentication (2FA)**: Implement two-factor authentication on RDP sessions. This adds an additional layer of security, making it significantly harder for attackers to gain unauthorized access even if they have compromised credentials.

By adopting these mitigation strategies, organizations can significantly bolster their defenses against RDP-related security threats.
