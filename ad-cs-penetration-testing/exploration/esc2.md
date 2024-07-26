---
description: >-
  Domain escalation via No Issuance Requirements + Enrollable Any Purpose EKU or
  no EKU
cover: ../../.gitbook/assets/Attacks by Service.png
coverY: 32.82133333333333
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

# 2️⃣ ESC2

#### ESC2 – Template Misconfiguration <a href="#esc2--template-misconfiguration-part-ii" id="esc2--template-misconfiguration-part-ii"></a>

In ESC2, the certificate template includes the “Any Purpose EKU” or “No EKU” options. EKU stands for “Extended/Enhanced Key Usage” and defines how a certificate can be utilized.&#x20;

These options allow the certificate to be used for any purpose, such as client or server authentication.&#x20;

Often, ESC2 can be combined with another ESC vulnerability to bypass restrictions on certificate usage, which can lead to privilege escalation by circumventing critical defenses.

The requirements for ESC2 include:

1. The Certificate Authority (CA) grants low-privileged users enrollment rights, this allows groups such as “Domain Users” to request certificates.
2. The certificate request is not required to be approved by a certificate “manager”.
3. Authorized signatures aren’t required, meaning that a pre-approved certificate does not need to be provided to issue a new certificate.
4. Includes the “Any purpose EKU”, or “No EKU” attribute.
