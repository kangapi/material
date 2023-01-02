## Remote Access
- Virtual Private Networks (VPN)
- Secure Shell (SSH)
- File Transfer Protocol (FTP)
- Virtual Network Computing (VNC)
- Windows Remote Management (or PowerShell Remoting) (WinRM)
- Remote Desktop Protocol (RDP)

``` bash title="Get window version"
PS C:\htb> Get-WmiObject -Class win32_OperatingSystem | select Version,BuildNumber

Version    BuildNumber
-------    -----------
10.0.19041 19041
``` 
``` bash title="Display graphically the directory structure"
PS C:\Users\htb-student> tree c:\ /f | more

Folder PATH listing
Volume serial number is 905B-28C3
C:\
├───75afac25577675a9bfafd2405602
├───Academy
│       flag.txt
│
├───PerfLogs
├───Program Files
│   ├───Common Files
│   │   ├───microsoft shared
│   │   │   ├───ink
│   │   │   │   │   Alphabet.xml
│   │   │   │   │   Content.xml
```
``` bash title="List NTFS permissions"
C:\htb> icacls c:\windows

c:\windows NT SERVICE\TrustedInstaller:(F)
           NT SERVICE\TrustedInstaller:(CI)(IO)(F)
           NT AUTHORITY\SYSTEM:(M)
           NT AUTHORITY\SYSTEM:(OI)(CI)(IO)(F)
           BUILTIN\Administrators:(M)
           BUILTIN\Administrators:(OI)(CI)(IO)(F)
           BUILTIN\Users:(RX)
           BUILTIN\Users:(OI)(CI)(IO)(GR,GE)
           CREATOR OWNER:(OI)(CI)(IO)(F)
           APPLICATION PACKAGE AUTHORITY\ALL APPLICATION PACKAGES:(RX)
           APPLICATION PACKAGE AUTHORITY\ALL APPLICATION PACKAGES:(OI)(CI)(IO)(GR,GE)
           APPLICATION PACKAGE AUTHORITY\ALL RESTRICTED APPLICATION PACKAGES:(RX)
           APPLICATION PACKAGE AUTHORITY\ALL RESTRICTED APPLICATION PACKAGES:(OI)(CI)(IO)(GR,GE)

Successfully processed 1 files; Failed processing 0 files
```
F: full access
D: delete access
N: no access
M: modify access
RX: read and execute access
R: read-only access
W : write-only access
### Remote Desktop Protocol (RDP)
Port 3389
!!! usage
    `xfreerdp /v:<targetIp> /u:htb-student /p:Password`
!!! example
    `xfreerdp /v:10.129.22.118 /u:htb-student /p: Academy WinFun!`

