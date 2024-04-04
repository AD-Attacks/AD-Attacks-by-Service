# Kerberos Documentation

* Understanding Kerberos Authentication: A Comprehensive Guide
* [Kerberos Silver Ticket Attack Explained](https://www.ad-attacks.com/silver-ticket-attack-explained/)
* [Kerberos Golden Ticket Attack Explained](https://www.ad-attacks.com/golden-ticket-attack-explained/)
* [Kerberos Diamond Ticket Attack Explained](https://www.ad-attacks.com/diamond-ticket-attack-explained/)
* [Understanding Pass-the-Ticket (PtT) Attacks: A Comprehensive Guide](https://www.ad-attacks.com/pass-the-ticket-ptt/)
* [Understanding Pass-the-Hash (PtH): A Comprehensive Explanation of an Exploitation Technique](https://www.ad-attacks.com/understanding-pass-the-hash-pth/)
* [What is Kerberoasting and How Security Experts Utilize It](https://www.ad-attacks.com/kerberoasting/)
* [AS-REP Roasting: A Comprehensive Guide for All Cyber Security Professionals](https://www.ad-attacks.com/as-rep-roasting/)

Kerberos authentication is a network authentication protocol designed to provide strong authentication for client/server applications by using secret-key cryptography.&#x20;

At its core, Kerberos is based on the Needham-Schroeder symmetric key protocol and was developed as part of MIT's Project Athena.&#x20;

The primary objective of Kerberos is to authenticate users to services and services to users in a secure and transparent manner, without the need for transmitting passwords over the network.

#### How Kerberos Works:

1. **Initial Authentication**: The user logs in, and the Kerberos client system sends a pre-authentication request to the Key Distribution Center (KDC), specifically to the Authentication Server (AS) component. The user’s password is used to encrypt this request.
2. **TGT Issuance**: Upon successful authentication, the AS responds with a Ticket-Granting Ticket (TGT), encrypted using a key derived from the user's password. The user’s system decrypts this TGT using the user's password and stores it for future use.
3. **Service Request**: When the user needs to access a service (e.g., a file server), the client requests a service ticket from the KDC's Ticket-Granting Service (TGS) using the TGT.

{% embed url="https://www.youtube.com/watch?v=snGeZlDQL2Q" %}
