---
description: Domain escalation via vulnerable PKI AD Object Access Control
---

# ESC5

### Domain Escalation via Vulnerable PKI AD Object Access Control

Domain escalation refers to the process of gaining elevated permissions within a domain, often leading to unauthorized access to sensitive data or control over domain resources. When a Public Key Infrastructure (PKI) within Active Directory (AD) has improperly configured Access Control Lists (ACLs), it might be vulnerable to exploitation, allowing attackers to escalate their domain privileges.

#### How It Works

1. **Identify Vulnerable PKI AD Object**: Attackers locate a PKI AD object with weak or misconfigured ACLs. This could be a Certificate Authority (CA) that doesn't properly restrict access.
2. **Exploiting ACLs**: Upon finding a vulnerable object, attackers manipulate the ACLs to grant themselves higher privileges or to execute commands that should be restricted.
3. **Privilege Escalation**: With elevated privileges, attackers can now access sensitive information, compromise accounts, or deploy malicious payloads within the domain.

#### Mitigation

To protect against this type of escalation:

* **Regularly Review ACLs**: Ensure that ACLs on PKI AD objects are correctly set, following the principle of least privilege.
* **Monitor AD Objects**: Use tools to monitor changes to AD objects and ACLs, alerting administrators of unauthorized modifications.
* **Implement Multi-Factor Authentication (MFA)**: Reduce the risk of initial compromise which could lead to escalation.
* **Security Training**: Educate administrators on the importance of secure ACL configurations and the risks associated with PKI within AD environments.
