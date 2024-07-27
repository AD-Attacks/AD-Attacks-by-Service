---
description: ESC12 – ADCS CA on YubiHSM
---

# 0️⃣ ESC12

Administrators can store an ADCS CA on a Yubico YubiHSM. If an adversary gains remote command execution of the host operating system, they can use the YubiHSM CA private key to create and issue certificates.&#x20;

This is possible by unlocking the YubiHSM using the plaintext password found in the registry key: `HKEY_LOCAL_MACHINE\SOFTWARE\Yubico\YubiHSM\AuthKeysetPassword`.

\
