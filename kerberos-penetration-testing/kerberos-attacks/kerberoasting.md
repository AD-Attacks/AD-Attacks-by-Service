---
description: >-
  Dive into our insightful article to understand Kerberoasting; its purpose,
  workings, and role in cybersecurity. Learn how to safeguard your digital
  assets!
---

# Kerberoasting

#### Kerberoasting

Kerberoasting is a type of attack against the Kerberos authentication protocol. It exploits how service accounts utilize Kerberos tickets (Service Principal Names - SPNs) to authenticate to various services in a network. Here's a simplified breakdown:

1. **Identifying Services**: Attackers enumerate accounts with SPNs set, as these represent services that can be requested.
2. **Ticket Request**: The attacker requests a Ticket-Granting Service (TGS) ticket for each identified service.
3. **Extraction and Cracking**: The TGS tickets, encrypted with the service account's password hash, are extracted from the attacker's memory. These can then be offline brute-forced to reveal the plaintext passwords.

The primary defense against Kerberoasting involves using strong, complex passwords for service accounts and monitoring for abnormal Kerberos activity.
