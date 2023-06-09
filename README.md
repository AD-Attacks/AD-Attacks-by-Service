[Home](https://docs.ad-attacks.com) | [About](./website/About.md) | [Projects](./website/Projects.md) | [Contact](./website/Contact.md)| [Discord](./website/Discord.md)| [Author](./website/Author.md)

# Active Directory Penetration Testing

Welcome to the Active Directory Attacks Documentation for Red Teams!

This documentation serves as a comprehensive resource for understanding various attack techniques and vulnerabilities associated with Active Directory environments. Whether you are a security professional, system administrator, or simply interested in learning about cybersecurity, this documentation will provide valuable insights into the risks and countermeasures related to Active Directory attacks.

In this documentation, you will find detailed explanations of different attack techniques employed by malicious actors to compromise Active Directory infrastructures. We cover well-known techniques such as Pass-the-Hash, Golden Ticket, Kerberoasting, and more. Each attack technique is accompanied by a description, potential impact, detection methods, and recommended mitigation strategies.
![Active Directory Penetration Testing!](https://cdn.ad-attacks.com/Active-Directory-Attacks.png "Active Directory Penetration Testing")

Our aim is to help you understand the inner workings of these attacks, enabling you to identify vulnerabilities within your own Active Directory environment and implement effective security measures to protect against them. Additionally, we provide real-world examples and practical guidance to enhance your understanding of the attack vectors and their implications.

We encourage you to explore the various sections of this documentation, where you will find detailed explanations, step-by-step guides, and recommended best practices to secure your Active Directory infrastructure. Stay one step ahead of potential threats and bolster your organization's security posture with the knowledge gained from this documentation.

Remember, a well-informed defender is better equipped to safeguard their Active Directory environment against malicious actors. Let's dive in and strengthen our defenses against Active Directory attacks!

Happy learning and stay secure!


<img src="https://cdn.ad-attacks.com/Active-Directory-Attacks.png" alt="Image Alt Text" style="width:1080px;height:720px;">




# Active-Directory-Penetration-Testing
Active Directory Penetration Testing for Red Teams


- [Author RFS](https://author.popdocs.net/)



## Learn Active Directory

| Header 1 | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Cell 1   | Cell 2   | Cell 3   |
| Cell 4   | Cell 5   | Cell 6   |
| Cell 7   | Cell 8   | Cell 9   |


## Scenarios

| Scenario | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Windows Client   | Cell 2   | Cell 3   |
| Windows Client with AD   | Cell 5   | Cell 6   |
| Windows Server Standalone   | Cell 8   | Cell 9   |
| Windows Server with AD   | Cell 8   | Cell 9   |


## Active Directory External Reconnaissance



## Active Directory Attacks Theory

### Initial Compromise
### Host Reconnaissance
### Host Exploiting
### Host Persistence
### Lateral Movement

## Active Directory Attacks by Service Type (Protocol)

- [NetBIOS](./NetBIOS)
- [DNS](./DNS/index.md) 
- [MsSQL](./MSSQL/index.md) 
- [LDAP](./LDAP/index.md)
- [Kerberos](./Kerberos/index.md)
- [Samba](./Samba/index.md)
- [IIS](./IIS/index.md)
- [Exchange](./Exchange/index.md)
- [WinRM](./WinRM/index.md)
- [SCCM](./SCCM/index.md)

## My Tools Arsenal Documentation
- [Nmap]()
- [CrackMapExec](https://crackmapexec.popdocs.net/)
- [Rubeus]()
- [Certify]()
- [Mimikatz]()
- [BloodHound](https://bloodhound.popdocs.net/)
- [DeathStar]()
- [Metasploit]()
- [Empire]()
- [Covenant]()
- [Cobal Strike]()


## Windows Privilege Escalation


## Domain Privilege Escalation

- Attack Privilege Requirements
- Kerbrute Enumeration — No domain access required
- Pass the Ticket — Access as a user to the domain required
- Kerberoasting — Access as any user required
- AS-REP Roasting — Access as any user required
- Golden Ticket — Full domain compromise (Domain Admin) required
- Silver Ticket — Service hash required
- Skeleton Key — Full domain compromise (Domain Admin) required

## AD Attacks
| Attack Technique        | Description                                                                                                                                                                       |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pass-the-Hash          | An attack where an attacker steals the hash of a user's password and uses it to authenticate and impersonate the user.                                                           |
| Golden Ticket          | A technique that allows an attacker to forge Kerberos tickets, granting them unauthorized access with domain-level privileges.                                                   |
| Kerberoasting          | Exploits the weak encryption of Kerberos ticket-granting tickets (TGTs) to extract the password hashes of Active Directory service accounts.                                       |
| BloodHound             | A tool used to identify and exploit Active Directory trust relationships, exposing potential attack paths and lateral movement opportunities.                                       |
| DCShadow               | An attack that manipulates domain controllers to create a rogue domain controller, allowing attackers to stealthily inject changes into the Active Directory infrastructure.           |
| Skeleton Key           | A technique that allows an attacker to bypass authentication by injecting a backdoor password into Active Directory, granting them unauthorized access.                          |
| Silver Ticket          | Similar to a Golden Ticket, but instead of compromising the Key Distribution Center (KDC), it targets specific service principals, granting unauthorized access to specific services. |

## Projects
Here are some of my notable projects:

- [PopLabSec](https://github.com/username/project1): Description of Project 1.
- [AD Attacks](https://github.com/username/project2): Description of Project 2.
- [Offensive Wireless](https://github.com/username/project3): Description of Project 3.
- [IoT Hacking 101](https://github.com/username/project3): Description of Project 3.
- [TelcoSec](https://github.com/username/project3): Description of Project 3.
- [PopLAb Linux](https://github.com/username/project3): Description of Project 3.
- [PopDocs](https://github.com/username/project3): Description of Project 3.

Feel free to explore these projects and provide any feedback or suggestions.


## More Documentation

- [Active Directory Penetration Testing](https://github.com/PopLabSec/Active-Directory-Penetration-Testing)
- [Infrastructure Penetration Testing]()
- [Networks Penetration Testing](https://github.com/PopLabSec/Networking-Penetration-Testing)
- [Web Applications Penetration Testing](https://github.com/PopLabSec/Web-Applications-Penetration-Testing)
- [Wireless Security](https://www.offensive-wireless.com/)
- [Ethical Hacking](https://github.com/PopLabSec/RFS-Ethical-Hacking)




## Certifications Guides


- [CRTO-Exam-Guide](https://github.com/PopLabSec/CRTO-Exam-Guide)
- [OSCP Study Guide 2023](https://github.com/PopLabSec/OSCP-Study-Guide-2023)
- [eJPT Study Guide](https://github.com/PopLabSec/eJPT-Study-Guide)
- [eCPPTv2 AIO](https://github.com/PopLabSec/eCPPTv2-AIO)
