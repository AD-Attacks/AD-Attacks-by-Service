# WinRM

### Active Directory Lateral Movement with WinRM

Lateral movement in a network, particularly in the context of an Active Directory (AD) environment, refers to the techniques attackers use to move through a network after gaining initial access. This enables them to reach their target, often high-value assets, without detection. One common method for lateral movement in AD environments is utilizing Windows Remote Management (WinRM).

#### What is WinRM?

WinRM is a Microsoft implementation of WS-Management Protocol - a standard protocol used for remote management. It is enabled by default on Windows Server 2012 and later, allowing administrators to remotely manage Windows machines using a secure web services-based protocol.

#### How it's used for Lateral Movement:

1. **Initial Access**: First, an attacker gains access to a single machine within the network. This can be achieved through phishing, exploitation of a vulnerability, or using stolen credentials.
2. **Enumeration**: Then, the attacker enumerates the AD environment to identify targets and understand the network structure. Tools like BloodHound can be used for this purpose.
3. **Credential Theft**: The attacker may steal credentials from the compromised machine using tools like Mimikatz. This could include user names, passwords, and Kerberos tickets.
4. **WinRM for Movement**: With valid credentials or tokens, an attacker uses WinRM to execute commands remotely on other machines within the network. This requires the attacker to have the necessary permissions on the target machine.
   * The command for remote execution typically looks like: `Invoke-Command -ComputerName TargetMachine -Credential $cred -ScriptBlock {Commands}`
5. **Expanding Control**: By repeating the process, the attacker can move laterally across the network, compromising additional systems and escalating their privileges.

#### Mitigation:

* Restrict and monitor the use of administrative privileges.
* Regularly update and patch systems to reduce vulnerabilities.
* Implement multi-factor authentication.
* Monitor and log activity on the network to detect unusual behavior.
* Disable WinRM where it is not needed, or strictly limit which users can use it.

By understanding how attackers exploit WinRM for lateral movement, organizations can better prepare defenses and reduce their attack surface within Active Directory environments.
