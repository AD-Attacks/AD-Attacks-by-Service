---
description: ESC13 - OID Group Link Abuse
---

# 0️⃣ ESC13

ESC13's impact largely depends on which Active Directory (AD) group the issuance policy is associated with. If it's linked to the Domain Admin group, it could enable full privilege escalation. The issuance policy includes an OID (Object Identifier) group link to an AD group, which ensures all AD objects are uniquely identifiable.

The certificate template has an issuance policy extension and requires specific conditions, such as client authentication and certificate enrollment. Unique to this vulnerability:

* If the certificate template allows enrollment for the current user or computer
* And the issuance policy has an OID group link

Then the user or computer can request a certificate allowing access to resources as a member of the specified group.

The OID group link attribute (ms-DS-OIDToGroup-Link) ties an issuance policy to a specific AD group, enabling this vulnerability.
