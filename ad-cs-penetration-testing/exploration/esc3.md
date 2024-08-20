---
description: >-
  Domain escalation via No Issuance Requirements + Certificate Request Agent EKU
  + no enrollment agent restrictions
coverY: 0
---

# 3️⃣ ESC3

ESC3 is quite similar to ESC1, but there is a key difference that sets it apart. The template for ESC3 includes the “Certificate Request Agent EKU” (Extended Key Usage) option.&#x20;

This feature is significant because it allows the certificate to be requested on behalf of another principal.&#x20;

For instance, an individual with the necessary permissions can request a certificate for another user, such as a Domain Admin.&#x20;

This capability is crucial for environments that require flexible and delegated certificate management, ensuring that the right certificates can be obtained by authorized proxies, enhancing both administrative efficiency and security.

The attack requirements for ESC3 include:

1. The Certificate Authority (CA) grants low-privileged users enrollment rights, this allows groups such as “Domain Users” to request certificates.
2. The certificate request is not required to be approved by a certificate “manager”.
3. Authorized signatures aren’t required, meaning that a pre-approved certificate does not need to be provided to issue a new certificate.
4. The template includes the “Certificate Request Agent EKU”, allowing the request of a certificate as a highly privileged user.

```
certipy req -u attacker -p 'P@ssw0rd' -target-ip 192.168.1.2 -ca 'lab-DC-CA' -template 'ESC3'
```

```
certipy req -u attacker -p 'P@ssw0rd' -target-ip 192.168.1.2 -ca 'lab-DC-CA' -template 'User' -on-behalf-of 'lab\administrator' -pfx 'attacker.pfx'
```

