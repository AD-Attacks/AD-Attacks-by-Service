---
description: NTLM Relay to AD CS HTTP Endpoints
---

# 8️⃣ ESC8

#### ESC8 Attack: NTLM Relay to AD CS HTTP Enrollment

ESC8 involves coercing a Domain Controller (DC) to send an authentication request using its computer account. This enables an NTLM relay attack targeting the AD CS HTTP enrollment endpoint, allowing the attacker to request a certificate as the DC's computer account, effectively gaining control over the domain.

An NTLM relay attack occurs when an adversary forces authentication from a device, user, or computer, and then relays that NTLM authentication request to another device, impersonating the user during authentication.

Active Directory Certificate Services (AD CS) offers certificate enrollment over HTTP through various web interfaces, which are typically not secured against NTLM relay attacks.

Active Directory Certificate Authorities that are vulnerable to ESC8 meet the following conditions:&#x20;

* NTLM authentication must be enabled.
* The enrollment service endpoint must be using HTTP.
* The CA must not be installed on the Domain Controller

Full Domain takeover is possible under these conditions. If the CA is installed on the DC, it allows for the takeover of any other Domain device.&#x20;

By coercing authentication from another device on the Domain, you can request a certificate as that account. With this certificate, shadow credentials or RBCD can be used to compromise the targeted machine.

\
