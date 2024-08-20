---
description: >-
  Discover the details in our in-depth article on Kerberos Attacks. Understand
  how they operate, techniques used by hackers and how to efficiently safeguard
  your systems.
cover: ../../.gitbook/assets/Attacks by Service.png
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

# 🟢 Kerberos Attacks

Kerberos is a network authentication protocol designed to provide strong authentication for client/server applications by using secret-key cryptography. Despite its robust design, several attack vectors have been identified and exploited by malicious actors.&#x20;

Understanding these attacks is crucial for cybersecurity professionals tasked with defending their networks. Below is an overview of some of the most common Kerberos-related attacks.

{% embed url="https://cli-ck.me/REdmV" %}

{% @mailchimp/mailchimpSubscribe %}

#### Kerberos Brute-Force Attack

A brute-force attack involves attempting numerous username and password combinations until a successful authentication occurs. While Kerberos itself is resistant to brute-force attacks due to its reliance on strong cryptographic techniques, attackers may still attempt to brute-force initial access or the decryption of intercepted Kerberos tickets by guessing the passwords of service accounts.

#### ASREPRoast

ASREPRoasting is an attack against Kerberos that targets accounts configured without pre-authentication. Since pre-authentication is not required, an attacker can request authentication data for any user, and then attempt to crack the encrypted part of the response offline, potentially revealing the user's password.

#### Kerberoasting

Kerberoasting exploits the TGS (Ticket Granting Service) aspect of Kerberos. It allows an attacker to crack the passwords of service accounts in a domain. By requesting TGS tickets for different services and then attempting to crack the encrypted portion of these tickets, attackers can potentially retrieve service account passwords in plaintext.

#### Pass the Key

Pass the Key (PtK) involves attackers leveraging stolen Kerberos keys (passwords, ticket-granting tickets, etc.) to authenticate to network resources as if they were the legitimate user. Unlike password-based attacks, PtK attacks use the cryptographic material directly, bypassing the need for password guessing or cracking.

#### Pass the Ticket

Pass the Ticket (PtT) is similar to Pass the Key but specifically involves the theft and reuse of Kerberos tickets. Attackers can extract ticket-granting tickets (TGTs) or service tickets from a compromised system and then use those tickets from another computer to gain unauthorized access to resources.

#### Silver Ticket

Silver ticket attacks involve the creation of forged service tickets (TGS tickets) using a service's NTLM hash. These forged tickets can be used to access specific services such as file servers, SharePoint, etc., without needing to compromise the entire Kerberos TGT process.

#### Golden Ticket

Golden ticket attacks are particularly insidious, involving the creation of a forged TGT ticket using the KRBTGT account's NTLM hash. With a golden ticket, an attacker gains unrestricted access to any resource within the Active Directory domain, essentially granting them "god mode" within the compromised environment.

Understanding and mitigating these attacks require a robust security posture, including regular auditing of service account permissions, enforcing the use of strong, unique passwords for service accounts, and implementing advanced monitoring and alerting for unusual authentication requests or patterns.

{% embed url="https://www.tarlogic.com/blog/how-to-attack-kerberos/" %}
