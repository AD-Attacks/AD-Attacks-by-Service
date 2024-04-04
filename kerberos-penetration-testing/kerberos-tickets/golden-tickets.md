# Golden Tickets

### Golden Tickets

Golden Tickets refer to a type of attack targeting Windows Active Directory environments.&#x20;

Here's a brief overview:

* **What Are They?** Golden Tickets are special authentication tickets that allow attackers to assume the identity of any user on the Active Directory once the Key Distribution Center's (KDC) secret key (used in the Kerberos protocol) is compromised.
* **How They Work:** By compromising the KDC, specifically the account for the domain controller (krbtgt), attackers can create tickets that grant them access to any resource within the domain.
* **Impact:** This type of attack grants attackers extensive lateral movement within a network and can remain undetected for a long duration, posing significant security risks.
* **Mitigation:** Regularly changing the krbtgt account password (twice to mitigate the use of an old password), implementing strict access controls, and monitoring unusual activities are key steps in mitigating Golden Ticket attacks.

{% embed url="https://www.youtube.com/watch?v=o98_eRt777Y" %}
