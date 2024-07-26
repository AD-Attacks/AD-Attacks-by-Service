---
description: No Security Extension
---

# 9️⃣ ESC9

When the enrollment flag `CT_FLAG_NO_SECURITY_EXTENSION` is set on a certificate that a user has enrollment permissions for, and another principal has GenericWrite over that user, this scenario can be exploited to request a certificate as any user in the Domain.

According to the Microsoft [Documentation](https://learn.microsoft.com/en-us/openspecs/windows\_protocols/ms-wcce/a1f27ffb-7f74-4fa1-8841-7cde4ba0bcfe) on the msPKI-Certificate-Name-Flag value:

```
If the CT_FLAG_NO_SECURITY_EXTENSION flag is not set, the CA MUST add the szOID_NTDS_CA_SECURITY_EXT security extension, as specified in section 2.2.2.7.7.4, to the issued certificate with the value set to the string format of the objectSid attribute obtained from the requestor’s user object in the working directory. For this, the CA MUST invoke the processing rules in section 3.2.2.1.2, with input parameter EndEntityDistinguishedName set equal to the requester's user object distinguished name, and retrieve the objectSid attribute from the returned EndEntityAttributes output parameter.
```

So when CT\_FLAG\_NO\_SECURITY\_EXTENSION is set, the CA never adds the szOID\_NTDS\_CA\_SECURITY\_EXT security extension, meaning it never directly references the users ObjectSid value.

We can change the user's UPN (User Principal Name) to that of a higher-privilege user, deliberately leaving the domain ambiguous to avoid conflicts. After altering the UPN, request a certificate as the spoofed user, then revert the UPN to its original value.
