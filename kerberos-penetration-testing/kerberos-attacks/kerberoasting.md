---
description: >-
  Dive into our insightful article to understand Kerberoasting; its purpose,
  workings, and role in cybersecurity. Learn how to safeguard your digital
  assets!
---

# Kerberoasting

### Kerberoasting

Kerberoasting is a type of attack against the Kerberos authentication protocol. It exploits how service accounts utilize Kerberos tickets (Service Principal Names - SPNs) to authenticate to various services in a network. Here's a simplified breakdown:

1. **Identifying Services**: Attackers enumerate accounts with SPNs set, as these represent services that can be requested.
2. **Ticket Request**: The attacker requests a Ticket-Granting Service (TGS) ticket for each identified service.
3. **Extraction and Cracking**: The TGS tickets, encrypted with the service account's password hash, are extracted from the attacker's memory. These can then be offline brute-forced to reveal the plaintext passwords.

The primary defense against Kerberoasting involves using strong, complex passwords for service accounts and monitoring for abnormal Kerberos activity.

### Defenses Against Kerberoasting

To bolster your network against Kerberoasting attacks, consider implementing the following measures:

1. **Strong Password Policies**: Enforce complex and unique passwords for all service accounts. Ideally, use passphrases that are longer and include a mix of characters.
2. **Regular Password Changes**: Rotate service account passwords frequently to minimize the window of opportunity for attackers.
3. **Monitor for Unusual Activity**: Implement logging and alerting for abnormal Kerberos ticket requests. Tools like Kerberos Monitoring and Security Information and Event Management (SIEM) solutions can help detect suspicious patterns.
4. **Least Privilege Principle**: Limit service account privileges to the minimum required for their function. This reduces the potential damage an attacker can cause if they compromise an account.
5. **Encryption and Tuning**: Ensure Kerberos Pre-Authentication is enabled to add an additional layer of security. Use newer encryption types for Kerberos to strengthen the protection of tickets.

By combining these strategies, organizations can significantly reduce the risk of successful Kerberoasting attacks.
