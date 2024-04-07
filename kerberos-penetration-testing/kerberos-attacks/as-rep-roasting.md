---
description: >-
  Explore our informative article on AS-REP Roasting, offering extensive
  insights and understanding about the mechanism leveraged in hacking
  methodologies. Understand and prevent potential threats.
---

# AS-REP Roasting

AS-REP Roasting is an attack method that targets Kerberos authentication within Windows environments. Kerberos, a network authentication protocol, is designed to offer strong authentication for client/server applications.&#x20;

AS-REP Roasting can be exploited when an account is configured to not require Kerberos pre-authentication.&#x20;

Without pre-authentication, an attacker can request an AS-REP (Authentication Service Response) for any user that has the pre-authentication disabled and attempt to crack the encrypted part of the response offline, aiming to retrieve the user’s credentials.&#x20;

This vulnerability can be mitigated by ensuring that all user accounts require Kerberos pre-authentication.
