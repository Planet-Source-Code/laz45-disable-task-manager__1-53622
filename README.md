<div align="center">

## Disable Task Manager


</div>

### Description

This code disables Task Manager in XP and I think other Operating Systems like Win2000
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Laz45](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/laz45.md)
**Level**          |Beginner
**User Rating**    |3.9 (47 globes from 12 users)
**Compatibility**  |VB 6\.0
**Category**       |[Registry](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/registry__1-36.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/laz45-disable-task-manager__1-53622/archive/master.zip)





### Source Code

<h6>Public Sub DisableTaskMgr()<BR>
Open "C:\X.reg" For Output As #1<BR>
Print #1, "Windows Registry Editor Version 5.00"<BR>
Print #1, ""<BR>
Print #1, _ "[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\System]"
Print #1, """DisableTaskMgr""" & "=dword:00000001"<BR>
Close #1<BR>
Shell ("Regedit /s C:\X.reg")<BR>
Kill "C:\X.reg"<BR>
End Sub</h6>

