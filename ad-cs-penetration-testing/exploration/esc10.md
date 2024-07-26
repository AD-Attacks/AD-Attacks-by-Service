---
description: Weak Certificate Mappings
---

# 🔟 ESC10

ESC10 is a variation of the technique used in ESC9 for Domain compromise. It involves using an account over which our current principal has GenericWrite permissions to compromise any account on the Domain, including a Domain Administrator.

The difference between ESC9 and ESC10 is that ESC9 is restricted to a specific template, whereas ESC10 is not.

There are two main exploitation pathways, identifiable by specific registry keys on the Domain Controller:

1. When StrongCertificateBindingEnforcement is configured as 0, this key is located at HKEY\_LOCAL\_MACHINE\SYSTEM\CurrentControlSet\Services\Kdc

To mirror ESC9, use a controlled user account and modify the UPN to request an Administrator certificate.

1. If CertificateMappingMethods includes the UPN bit (0x4), this key is located at HKEY\_LOCAL\_MACHINE\System\CurrentControlSet\Control\SecurityProviders\Schannel.

The second method is slightly different, enabling us to compromise any account that lacks the userPrincipalName property via the proxy account with GenericWrite permissions.

This includes Machine Accounts like Domain Controllers.
