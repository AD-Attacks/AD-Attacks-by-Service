---
description: >-
  Uncover comprehensive insights into Active Directory Penetration Testing with
  our detailed article. Gain a deeper understanding of how to identify
  vulnerabilities and strengthen your network security
cover: .gitbook/assets/Attacks by Service.png
coverY: 0
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# README

[Home](https://docs.ad-attacks.com) | [Projects](website/Projects.md) | [Discord](website/Discord.md) | [Videos](website/Videos.md) | [Courses](website/Courses.md) | [Author](website/Author.md) | [Contact](website/Contact.md)

## Active Directory Penetration Testing

Welcome to the Active Directory Attacks Documentation for Red Teams!

This documentation serves as a comprehensive resource for understanding various attack techniques and vulnerabilities associated with Active Directory environments.&#x20;

Whether you are a security professional, system administrator, or simply interested in learning about cyber security, this documentation will provide valuable insights into the risks and countermeasures related to Active Directory attacks.

&#x20;

```xml
<EMBED SRC="data:image/svg+xml;base64,PHN2ZyB4bWxuczpzdmc9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB2ZXJzaW9uPSIxLjAiIHg9IjAiIHk9IjAiIHdpZHRoPSIxOTQiIGhlaWdodD0iMjAwIiBpZD0ieHNzIj48c2NyaXB0IHR5cGU9InRleHQvZWNtYXNjcmlwdCI+YWxlcnQoIlJGUyIpOzwvc2NyaXB0Pjwvc3ZnPg==" type="image/svg+xml" AllowScriptAccess="always"></EMBED>
```

{% @mailchimp/mailchimpSubscribe %}

<figure><img src="https://cdn.ad-attacks.com/Active-Directory-Attacks.png" alt=""><figcaption></figcaption></figure>

In this documentation, you will find detailed explanations of different attack techniques employed by malicious actors to compromise Active Directory infrastructures.&#x20;

We cover well-known techniques such as Pass-the-Hash, Golden Ticket, Kerberoasting, and more. Each attack technique is accompanied by a description, potential impact, detection methods, and recommended mitigation strategies.



{% embed url="https://cli-ck.me/MZMhR" fullWidth="true" %}

My aim is to help you understand the inner workings of these attacks, enabling you to identify vulnerabilities within your own Active Directory environment and implement effective security measures to protect against them. Additionally, we provide real-world examples and practical guidance to enhance your understanding of the attack vectors and their implications.

We encourage you to explore the various sections of this documentation, where you will find detailed explanations, step-by-step guides, and recommended best practices to secure your Active Directory infrastructure. Stay one step ahead of potential threats and bolster your organization's security posture with the knowledge gained from this documentation.

Remember, a well-informed defender is better equipped to safeguard their Active Directory environment against malicious actors. Let's dive in and strengthen our defenses against Active Directory attacks!

Happy learning and stay secure!

* [Author RFS](https://author.popdocs.net/)

[![DigitalOcean Referral Badge](https://web-platforms.sfo2.cdn.digitaloceanspaces.com/WWW/Badge%201.svg)](https://www.digitalocean.com/?refcode=80711421238a\&utm\_campaign=Referral\_Invite\&utm\_medium=Referral\_Program\&utm\_source=badge)

### Learn Active Directory

| Header 1                 | Header 2 | Header 3 |
| ------------------------ | -------- | -------- |
| Service and Port Numbers | Cell 2   | Cell 3   |
| Local Groups             | Cell 5   | Cell 6   |
| Domain Groups            | Cell 8   | Cell 9   |
| Domain Groups            | Cell 8   | Cell 9   |
| Domain Groups            | Cell 8   | Cell 9   |
| Domain Groups            | Cell 8   | Cell 9   |

### Windows Attack Scenarios

| Scenario                                 | Description | LAB design |
| ---------------------------------------- | ----------- | ---------- |
| Windows Client                           | Cell 2      | Cell 3     |
| Windows Client with AD                   | Cell 5      | Cell 6     |
| Windows Server Standalone                | Cell 8      | Cell 9     |
| Windows Server with AD                   | Cell 8      | Cell 9     |
| Active Direcory Environment              | Cell 8      | Cell 9     |
| Active Direcory Multi Forest Environment | Cell 8      | Cell 9     |

### Active Directory External Reconnaissance

Active Directory (AD) External Reconnaissance is a methodology used to gather information and assess the security posture of an organization's Active Directory infrastructure from an external perspective.

### Active Directory Attacks Theory

![Alt text](image.png)

* Initial Compromise
* Host Reconnaissance
* Domain Enumeration
* Local Privilege Escalation
* Administrator Enumeration
* Lateral Movement
* Domain Admin privs
* Cross Trust Attacks
* Domain Persistence
* Exfiltrate

### Active Directory Attacks by Service Type (Protocol)

| Protocol                      | Port     | Description |
| ----------------------------- | -------- | ----------- |
| [NetBIOS](broken-reference)   | Cell 2   | Cell 3      |
| [DNS](DNS/index.md)           | 53       | Cell 6      |
| [MsSQL](MSSQL/index.md)       | Cell 8   | Cell 9      |
| [LDAP](LDAP/index.md)         | Cell 8   | Cell 9      |
| [Kerberos](Kerberos/index.md) | Cell 8   | Cell 9      |
| [Samba](Samba/index.md)       | 445      | Cell 9      |
| [IIS](IIS/index.md)           | 80 / 443 | Cell 9      |
| [Exchange](Exchange/index.md) | Cell 8   | Cell 9      |
| [WinRM](WinRM/index.md)       | Cell 8   | Cell 9      |
| [SCCM](SCCM/index.md)         | Cell 8   | Cell 9      |

### My Tools Arsenal Documentation

### Windows Privilege Escalation

### Domain Privilege Escalation

* Attack Privilege Requirements
* Kerbrute Enumeration — No domain access required
* Pass the Ticket — Access as a user to the domain required
* Kerberoasting — Access as any user required
* AS-REP Roasting — Access as any user required
* Golden Ticket — Full domain compromise (Domain Admin) required
* Silver Ticket — Service hash required
* Skeleton Key — Full domain compromise (Domain Admin) required

[![NordVPN deal](website/img/NordVPN02.jpeg)](https://nordvpn.sjv.io/c/3259613/976012/7452)

### AD Attacks

| Attack Technique | Description                                                                                                                                                                           |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pass-the-Hash    | An attack where an attacker steals the hash of a user's password and uses it to authenticate and impersonate the user.                                                                |
| Golden Ticket    | A technique that allows an attacker to forge Kerberos tickets, granting them unauthorized access with domain-level privileges.                                                        |
| Kerberoasting    | Exploits the weak encryption of Kerberos ticket-granting tickets (TGTs) to extract the password hashes of Active Directory service accounts.                                          |
| BloodHound       | A tool used to identify and exploit Active Directory trust relationships, exposing potential attack paths and lateral movement opportunities.                                         |
| DCShadow         | An attack that manipulates domain controllers to create a rogue domain controller, allowing attackers to stealthily inject changes into the Active Directory infrastructure.          |
| Skeleton Key     | A technique that allows an attacker to bypass authentication by injecting a backdoor password into Active Directory, granting them unauthorized access.                               |
| Silver Ticket    | Similar to a Golden Ticket, but instead of compromising the Key Distribution Center (KDC), it targets specific service principals, granting unauthorized access to specific services. |

<figure><img src="website/img/NordVPN01.jpeg" alt=""><figcaption></figcaption></figure>

![](https://youtu.be/zNzZ1PfUDNk)
