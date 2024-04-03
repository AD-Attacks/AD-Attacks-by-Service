---
coverY: 0
---

# SPN-Jacking

#### SPN-Jacking

SPN-Jacking is a security exploit technique that targets the Service Principal Name (SPN) in a Microsoft Active Directory environment. An SPN is a unique identifier for a service instance on a network, used in Kerberos authentication.&#x20;

When a client wants to access a service, it requests a Kerberos ticket using the SPN of the service.

In an SPN-Jacking attack, an attacker exploits misconfigurations or vulnerabilities to register a rogue SPN in the Active Directory. This allows the attacker to impersonate legitimate services and perform man-in-the-middle (MitM) attacks, intercepting and possibly modifying the data exchanged between clients and services.&#x20;

This type of attack can lead to unauthorized access to sensitive information and potentially full domain compromise.

Preventing SPN-Jacking involves regularly auditing SPNs for any anomalies, monitoring for unauthorized SPN modifications, and implementing strict permissions for SPN registrations.
