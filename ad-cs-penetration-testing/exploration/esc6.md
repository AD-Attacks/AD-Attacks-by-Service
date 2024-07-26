---
description: >-
  Domain escalation via the EDITF_ATTRIBUTESUBJECTALTNAME2 setting on CAs + No
  Manager Approval + Enrollable Client Authentication/Smart Card Logon OID
  templates
---

# 6️⃣ ESC6

ESC6 involves abusing the “EDITF\_ATTRIBUTESUBJECTALTNAME2” flag on the Certification Authority’s (CA) configuration.&#x20;

By enabling this flag, an attacker can exploit a significant vulnerability that allows any client to request a certificate with a different Subject Alternative Name (SAN).&#x20;

This malicious request essentially permits the client to impersonate any user or service within the domain, a severe breach of security.

The primary risk associated with this exploitation is the potential for domain privilege escalation. The attacker can strategically request a certificate that effectively grants them the identity of the Domain Administrator.&#x20;

With such escalated privileges, they can conduct a range of actions, including altering domain policies, accessing sensitive data, creating additional administrator accounts for sustained access, or even disrupting services.

The problem lies in the inability of the CA to correctly verify and validate SAN attributes when the “EDITF\_ATTRIBUTESUBJECTALTNAME2” flag is abused.&#x20;

This oversight can be leveraged to establish an unauthorized yet legitimate-looking certificate, circumventing standard security measures.

To mitigate this risk, it is crucial to review and tighten CA configurations, specifically scrutinizing the settings around SAN attribute requests.&#x20;

Regular audits and monitoring for unusual certificate requests, combined with strict access controls and enforcement of least privilege principles, can substantially reduce the window of opportunity for such attacks.

\
