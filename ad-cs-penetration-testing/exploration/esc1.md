---
description: >-
  Domain escalation via No Issuance Requirements + Enrollable Client
  Authentication/Smart Card Logon OID templates +
  CT_FLAG_ENROLLEE_SUPPLIES_SUBJECT
cover: ../../.gitbook/assets/Attacks by Service.png
coverY: 36.68266666666666
layout:
  cover:
    visible: true
    size: hero
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 1️⃣ ESC1

Templates vulnerable to ESC1 have the following configurations:

* Client Authentication: True
* Enabled: True
* Enrollee Supplies Subject: True
* Requires Management Approval: False
* Authorized Signatures Required: 0

**ESC1 Requirement 1: An overly permissive certificate template security descriptor grants certificate enrollment rights to low-privileged users.**

**ESC1 Requirement 2: The certificate template allows requesters to specify a subjectAltName in the CSR.**

**ESC1 Requirement 3: The certificate template defines EKUs that enable client authentication.**

**ESC1 Requirement 4: Manager approval is disabled.**

**ESC1 Requirement 5: No authorized signatures are required.**

\
\


\


>
>
> \
> SpectorOps
