# Update-CWCSessionName
## SYNOPSIS
Updates the name of a session.
## SYNTAX
```powershell
Update-CWCSessionName [-Server] <Object> [-GUID] <Object> [-User] <Object> [-Password] <Object> [[-NewName] <String>] [<CommonParameters>]
```
## DESCRIPTION
Updates the name of a session on the control server.
## PARAMETERS
### -Server &lt;Object&gt;
The address to your Control server. Example 'https://control.labtechconsulting.com' or 'http://control.secure.me:8040'
```
Required                    true
Position                    1
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -GUID &lt;Object&gt;
The GUID/SessionID for the machine you wish to connect to.

You can retreive session info with the 'Get-CWCSessions' commandlet



On Windows clients, the launch parameters are located in the registry at:

  HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\ScreenConnect Client (xxxxxxxxxxxxxxxx)\ImagePath

On Linux and Mac clients, it's found in the ClientLaunchParameters.txt file in the client installation folder:

  /opt/screenconnect-xxxxxxxxxxxxxxxx/ClientLaunchParameters.txt
```
Required                    true
Position                    2
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -User &lt;Object&gt;
User to authenticate against the Control server.
```
Required                    true
Position                    3
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -Password &lt;Object&gt;
Password to authenticate against the Control server.
```
Required                    true
Position                    4
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
### -NewName &lt;String&gt;
The new name for the session.
```
Required                    false
Position                    5
Default value
Accept pipeline input       false
Accept wildcard characters  false
```
## EXAMPLES
### EXAMPLE 1
```powershell
PS C:\>Update-CWCSessionName -Server $Server -GUID $GUID -User $User -Password $Password -NewName 'Session1'

Will rename the session to Session1
```

## NOTES
Version:        1.1

Author:         Chris Taylor

Creation Date:  10/25/2018

Purpose/Change: Initial script development 
