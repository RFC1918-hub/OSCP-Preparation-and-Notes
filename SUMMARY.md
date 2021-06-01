# Table of contents

* [Initial page](README.md)

## Reconnaissance and Pre Exploitation <a id="reconnaissance-and-post-exploitation"></a>

* [Enumerations](reconnaissance-and-post-exploitation/enumerations/README.md)
  * [nmap](reconnaissance-and-post-exploitation/enumerations/nmap.md)
  * [Network Discovery](reconnaissance-and-post-exploitation/enumerations/network-discovery/README.md)
    * [Banner grabbing \(without nmap\)](reconnaissance-and-post-exploitation/enumerations/network-discovery/banner-grabbing-without-nmap.md)
    * [Ports discovery \(without nmap\)](reconnaissance-and-post-exploitation/enumerations/network-discovery/ports-discovery-without-nmap.md)
    * [Ping Sweep](reconnaissance-and-post-exploitation/enumerations/network-discovery/ping-sweep.md)
  * [Common Ports and Services](reconnaissance-and-post-exploitation/enumerations/services/README.md)
    * [Port 111 - RpcBind](reconnaissance-and-post-exploitation/enumerations/services/rpcbind.md)
    * [Port 445 - SMB](reconnaissance-and-post-exploitation/enumerations/services/smb.md)

## Exploitations

* [SQLi](exploitations/sqli/README.md)
  * [MySQL](exploitations/sqli/sqli.md)
  * [Oracle](exploitations/sqli/oracle.md)
  * [MSSQL](exploitations/sqli/mssql.md)
* [Cross-Compiling Exploit Code](exploitations/cross-compiling-exploit-code.md)
* [Windows](exploitations/windows/README.md)
  * [AV Bypassing](exploitations/windows/av-bypassing.md)
  * [Run-As](exploitations/windows/run-as.md)
  * [Windows CVE Exploits](exploitations/windows/windows-cve-exploits/README.md)
    * [Eternal Blue](exploitations/windows/windows-cve-exploits/eternal-blue.md)
    * [MS16-135 - win32k.sys NtSetWindowLongPtr](exploitations/windows/windows-cve-exploits/ms16-135-win32k.sys-ntsetwindowlongptr.md)
  * [Windows Binary Compression and exe2hex](exploitations/windows/windows-tips-and-tricks.md)
  * [adduser.c code](exploitations/windows/adduser.c-code.md)
* [Reverse Shells](exploitations/reverse-shells/README.md)
  * [Linux](exploitations/reverse-shells/linux/README.md)
    * [Stabilize ZSH shell](exploitations/reverse-shells/linux/stabilize-zsh-shell.md)
    * [Fixing TTY](exploitations/reverse-shells/linux/fixing-tty.md)
  * [PowerShell](exploitations/reverse-shells/powershell.md)
* [Web Exploitation](exploitations/web-exploitation/README.md)
  * [Local File Inclusion \(LFI\)](exploitations/web-exploitation/lfi.md)

## Credentials

* [Mimikatz](credentials/mimikatz.md)

## Post Exploitation

* [PEAS](post-exploitation/peas/README.md)
  * [linpeas.sh](post-exploitation/peas/linpeas.sh.md)
  * [winPEAS](post-exploitation/peas/winpeas.md)
* [Connecting to a Target](post-exploitation/connecting-to-a-target/README.md)
  * [Windows](post-exploitation/connecting-to-a-target/windows/README.md)
    * [Remote Desktop Protocol](post-exploitation/connecting-to-a-target/windows/remote-desktop-protocol.md)
* [File Exfiltration and Transfers](post-exploitation/file-exfiltration-and-transfers/README.md)
  * [nc](post-exploitation/file-exfiltration-and-transfers/nc.md)
  * [socat](post-exploitation/file-exfiltration-and-transfers/socat.md)
  * [Windows](post-exploitation/file-exfiltration-and-transfers/windows/README.md)
    * [VBScript wget](post-exploitation/file-exfiltration-and-transfers/windows/vbscript-wget.md)
    * [Downloading File using Powershell and IEX](post-exploitation/file-exfiltration-and-transfers/windows/downloading-file-using-powershell-and-iex.md)
    * [File transfer over SMB](post-exploitation/file-exfiltration-and-transfers/windows/file-transfer-over-smb.md)
    * [powercat](post-exploitation/file-exfiltration-and-transfers/windows/powercat.md)
* [Windows Privilege Escalation](post-exploitation/windows-privilege-escalation/README.md)
  * [Kernel Exploits](post-exploitation/windows-privilege-escalation/kernel-exploits.md)
  * [Admin to SYSTEM](post-exploitation/windows-privilege-escalation/admin-to-system.md)
  * [Searching for Passwords in REG](post-exploitation/windows-privilege-escalation/searching-for-passwords-in-reg.md)
  * [accesschk.exe](post-exploitation/windows-privilege-escalation/accesschk.exe.md)
* [Linux Privilege Escalation](post-exploitation/linux-privilege-escalation.md)

## Pivoting

* [SSH](pivoting/ssh/README.md)
  * [SSH Reverse Tunnel](pivoting/ssh/ssh-reverse-tunnel.md)

## Buffer Overflows

* [Windows](buffer-overflows/windows/README.md)
  * [Stack Buffer Overflow](buffer-overflows/windows/stack-buffer-overflow.md)

