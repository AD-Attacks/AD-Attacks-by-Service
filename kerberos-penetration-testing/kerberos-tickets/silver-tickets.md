# ✅ Silver Tickets

### Silver Tickets

Silver Tickets are a type of security attack in Windows environments that target Kerberos, a network authentication protocol.&#x20;

They allow attackers to generate tickets granting access to specific services without requiring validation from the Key Distribution Center (KDC).



{% @mailchimp/mailchimpSubscribe %}

#### How They Work:

* **Exploitation:** An attacker must first compromise a service account to extract its password hash.
* **Ticket Creation:** With the hash, the attacker crafts a ticket granting ticket (TGT) for themselves, bypassing the need for actual authentication.
* **Access Granted:** The crafted TGT, or Silver Ticket, then grants access to the targeted service, allowing unauthorized actions.

#### Impact:

* Allows unauthorized access to services.
* Can be difficult to detect due to bypassing standard authentication checks.

#### Prevention:

* Regularly change service account passwords.
* Monitor for unusual activity within the network.
* Implement multi-factor authentication and limited permissions where possible.

{% embed url="https://www.youtube.com/watch?v=_nJ-b1UFDVM" %}
