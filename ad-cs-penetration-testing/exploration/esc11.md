---
description: ESC11 – Relaying NTLM to ICPR
---

# 0️⃣ ESC11

Consider that this could result in a full domain takeover. Similar to ESC8, if the CA is not hosted on the Domain Controller and authentication can be coerced, we can request a certificate for the DC machine account.&#x20;

By leveraging authentication coercion, we can relay any domain computer's authentication request to the CA and request a user certificate for that machine account, granting access to any machine on the domain.&#x20;

If the CA server lacks the “IF\_ENFORCEENCRYPTICERTREQUEST” attribute, an attacker can perform NTLM relay attacks to the RPC service without signing.

\
