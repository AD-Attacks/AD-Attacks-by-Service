# NTLM Authentication

NTLM (NT LAN Manager) authentication is a suite of Microsoft security protocols intended to provide authentication, integrity, and confidentiality to users.&#x20;

NTLM is utilized within a network when a client wishes to authenticate to a network server, relying on a domain controller to store and authenticate usernames and passwords using the following process:

1. **Negotiation**: The client sends a negotiation message to the server, indicating it wants to authenticate using NTLM.
2. **Challenge**: The server generates a random number (challenge) and sends it back to the client. This ensures that the response is unique and fresh.
3. **Authentication**: The client encrypts this challenge with the hash of the user's password and sends it back to the server. Additionally, the client sends the MD4 hash of the user's password (NTLM) or both the MD4 hash and a random number (NTLMv1, NTLMv2), depending on the version.
4. **Verification**: The server forwards the response to the domain controller. The domain controller checks the response against its database. If it matches, the authentication is considered successful.

NTLM does not natively support mutual authentication, where both the client and server verify each other's identity. It primarily uses symmetric key cryptography, where the same key is used for both encrypting and decrypting messages.&#x20;

NTLM's reliance on the domain controller as a trusted third party facilitates centralized management and enhances security within Windows environments.

#### **Hash Protocol Comparison**

| **Hash/Protocol** | **Cryptographic technique**                          | **Mutual Authentication** | **Message Type**                | **Trusted Third Party**                         |
| ----------------- | ---------------------------------------------------- | ------------------------- | ------------------------------- | ----------------------------------------------- |
| `NTLM`            | Symmetric key cryptography                           | No                        | Random number                   | Domain Controller                               |
| `NTLMv1`          | Symmetric key cryptography                           | No                        | MD4 hash, random number         | Domain Controller                               |
| `NTLMv2`          | Symmetric key cryptography                           | No                        | MD4 hash, random number         | Domain Controller                               |
| `Kerberos`        | Symmetric key cryptography & asymmetric cryptography | Yes                       | Encrypted ticket using DES, MD5 | Domain Controller/Key Distribution Center (KDC) |

#### **LAN Manager (LM or LANMAN)**

LAN Manager, often abbreviated as LM or LANMAN, is an early Microsoft client-server software that facilitates network operations. It's a network operating system (NOS) that Microsoft and 3Com Corporation developed for supporting enterprise-level networks.

* **Design and Usage**: LAN Manager was designed to manage and facilitate file and print sharing among networked computers. It provided critical infrastructure for early Windows and OS/2 networks.
* **Security**: In terms of security, LM was considered less secure because it stored passwords in a way that was relatively easy to decrypt. The LM hash is known for its vulnerability to brute force attacks due to its handling of passwords (splitting them into two 7-character halves and hashing separately).
* **Legacy and Evolution**: Although superseded by more secure protocols like NTLM (New Technology LAN Manager) and later Kerberos in Active Directory environments, LM played a foundational role in the development of Microsoft's network services. NTLM was introduced with Windows NT to address LM's security deficiencies, marking the beginning of its phase-out in modern network environments.

LAN Manager represents an important piece of network history, showcasing the evolution of authentication and security practices over time.



{% hint style="info" %}
Windows operating systems prior to Windows Vista and Windows Server 2008 (Windows NT4, Windows 2000, Windows 2003, Windows XP) stored both the LM hash and the NTLM hash of a user's password by default.
{% endhint %}

#### NTHash (NTLM)

NT Hash, often referred to as the NTLM hash, is a part of Microsoft's NTLM (New Technology LAN Manager) protocol, which succeeded the less secure LAN Manager (LM) protocol. Unlike its predecessor, NTLM provides more robust security features:

* **Encryption**: Utilizes MD4 hashing algorithm to create a 128-bit hash of the user's password. This method is significantly more secure than the LM hash.
* **Storage**: The NT hash is stored in the Security Account Manager (SAM) database or in Active Directory, providing a centralized and secure location for credential data.
* **Compatibility**: While designed to enhance security, NTLM maintains backward compatibility with systems that still use LM, though it's recommended to disable LM whenever possible to prevent its vulnerabilities from being exploited.

NTLM is part of a suite of authentication protocols that also includes Kerberos, offering a scalable and secure solution for modern Windows networks. However, in security-focused environments, Kerberos is preferred over NTLM due to its superior security mechanisms and reliance on mutual authentication and ticketing systems.
