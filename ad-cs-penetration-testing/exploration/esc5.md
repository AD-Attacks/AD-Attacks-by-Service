---
description: Domain escalation via vulnerable PKI AD Object Access Control
---

# 5️⃣ ESC5

### Domain Escalation via Vulnerable PKI AD Object Access Control

Domain escalation refers to the process of gaining elevated permissions within a domain, often leading to unauthorized access to sensitive data or control over domain resources. When a Public Key Infrastructure (PKI) within Active Directory (AD) has improperly configured Access Control Lists (ACLs), it might be vulnerable to exploitation, allowing attackers to escalate their domain privileges.

#### How It Works

1. **Identify Vulnerable PKI AD Object**: Attackers locate a PKI AD object with weak or misconfigured ACLs. This could be a Certificate Authority (CA) that doesn't properly restrict access.
2. **Exploiting ACLs**: Upon finding a vulnerable object, attackers manipulate the ACLs to grant themselves higher privileges or to execute commands that should be restricted.
3. **Privilege Escalation**: With elevated privileges, attackers can now access sensitive information, compromise accounts, or deploy malicious payloads within the domain.

This is mainly due to the fact that with control over the AD PKI, we can create specific conditions for any ESC vulnerability that allows Domain privilege escalation.

Some of the various objects include:

1. The CA’s Computer Object
2. The CA’s RPC/DCOM server
3. Any objects inside of the container “CN=Public Key Services,CN=Services,CN=Configuration,DC=,DC=”

