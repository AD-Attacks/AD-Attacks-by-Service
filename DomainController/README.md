# DomainController

### Active Directory Local Enumeration

On this chapter we will learn all about local enumeration inside an Active Directory.

* Enumerate Local Users
* Enumerate Domain Users
* Enumerate Shares
* Enumerate Password Policies
* Enumerate Active Sessions

### Active Directory Domain Enumeration

* [Enumerate Groups](./)
* [Enumerate Domains](https://www.poplabsec.com/active-directory-enumerate-domains/)
* [Enumerate GPOs](https://www.poplabsec.com/active-directory-enumerate-group-policy-objects/)
* [Enumerate OUs](./)
* [Enumerate ACLs](./)
* [Enumerate](./)
* [Enumerate Forests](./)
* [Enumerate Anti virus](./)

### Active Directory Remote Enumeration

Enumerate without Credentials

* Public Shares
* Null Sessions
* MiTM / Spoofing

#### Active Directory Privilege Escalation

* **Kerberoasting**: Exploit weak service account passwords by requesting TGS tickets and then cracking them offline.
* **Pass-the-Hash**: Utilize captured NTLM hashes to authenticate as the user without needing the plaintext password.
* **Golden Ticket**: Create a ticket granting ticket (TGT) with a forged PAC, allowing unrestricted access to any resource within the AD environment.
* **Silver Ticket**: Forge service-specific tickets (TGS) for accessing specific services without a valid TGT, bypassing TGT-based monitoring.
* **DCSync**: Mimic the behavior of a Domain Controller to pull password data from the AD database directly.

### Active Directory Exploits

* **EternalBlue CVE-2017-0144**: Exploit a vulnerability in Microsoft's SMBv1 protocol to achieve remote code execution.
* **Zerologon CVE-2020-1472**: Exploit a flaw in the Netlogon protocol allowing attackers to hijack Windows domain controllers and gain administrative access.
* **PrintNightmare CVE-2021-34527**: Exploit vulnerabilities in the Windows Print Spooler service to execute remote code with system privileges.



### Active Directory Password Attacks

* **Brute Force**: Attempt to guess passwords through rapid trial-and-error.
* **Password Spraying**: Attempt to access a large number of accounts with commonly used passwords.
* **Phishing**: Trick users into divulging their credentials through deceptive emails or websites.

### Lateral Movement Techniques in Active Directory

Lateral movement within an Active Directory environment involves techniques that allow an attacker to move from one compromised host to another.&#x20;

This phase is critical for expanding control within a network, gaining access to more resources, and achieving the ultimate goal of the attack. Some common techniques include:

#### **Pass-The-Ticket**

Pass-The-Ticket (PTT) technique involves the use of Kerberos tickets to authenticate to various services within the network without the need for user credentials. This technique exploits the way Kerberos authentication and session management are implemented in Windows networks.

#### **Overpass-The-Hash**

Similar to the Pass-The-Hash technique but specifically targets the Kerberos authentication protocol. Overpass-The-Hash involves taking a user's NTLM hash and using it to request a valid Kerberos ticket from the domain controller. This ticket can then be used to access resources within the Active Directory environment.

#### **Kerberoasting**

Kerberoasting exploits the Kerberos TGS (Ticket Granting Service) ticket system to crack the passwords of service accounts in the Active Directory. Attackers request TGS tickets for different services and then attempt to crack the tickets offline to reveal service account passwords.

### Active Directory Defense Evasion

Attackers often take steps to evade detection and maintain their foothold in a compromised Active Directory environment. Common defense evasion tactics include:

**Disabling Security Tools**

Attackers may attempt to disable or circumvent security software on the compromised hosts to avoid detection and maintain persistence.

**Modification of Group Policies**

By altering Group Policies, attackers can change security settings across the network, affecting how audits, alerts, and policies are applied to systems, potentially allowing malicious activity to go unnoticed.



### Session Passing Techniques

#### Beacon Passing

#### Foreign Listener

#### Spawn & Inject

### Active Directory Persistence

### Active Directory BYODC

### Build Infrastructure to Attack Active Directories

### **Active Directory Defense Techniques**

To safeguard your Active Directory environment against various attack techniques, it's imperative to employ robust defense mechanisms. Here are essential strategies for enhancing your Active Directory security posture:

* **Regularly Update and Patch**: Ensure that all systems are up-to-date with the latest security patches, particularly those within the Active Directory environment.
* **Least Privilege Access Model**: Implement the principle of least privilege, ensuring users only have the access rights essential for their roles.
* **Monitor and Audit**: Continuously monitor and audit Active Directory for any anomalous activities or changes, employing advanced security information and event management (SIEM) tools.
* **Use Multi-Factor Authentication (MFA)**: Enhance security by requiring more than one form of authentication, significantly reducing the risk of unauthorized access.
* **Deploy Advanced Threat Protection Solutions**: Implement solutions designed to detect, investigate, and respond to advanced threats within the Active Directory ecosystem.
* **Educate Users**: Regularly train users on the importance of following best security practices, such as recognizing phishing attempts and securing their credentials.

By incorporating these defensive strategies, organizations can significantly reduce their vulnerability to attacks targeting their Active Directory infrastructure.
