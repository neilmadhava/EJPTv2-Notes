# Mapping Network

- `fping -I <interface> -g <cidr_range> -a 2>/dev/null`
- `arp-scan -I <interface> -g <cidr_range>`
- https://catonmat.net/tcp-port-scanner-in-bash : bash tcp scan

```bash
#!/bin/bash
for port in {1..1000}; do
	timeout 1 bash -c "echo >/dev/tcp/$1/$port" 2>/dev/null && echo "port $port is open"
done
```		

## Nmap

- `nmap -sn <cidr_rage>` : ping scan like fping
	- -sV : service enumeration
	- -O : OS scan
	- -sC : default script scan
	- -Pn : treat hosts as online - skip hpst discovery
	- -sU : udp port scan
	- -iL <input file>: input hosts in file
- `nmap <ip> -p1-250 -sUV`
- `nmap <ip> -p 134 -sUV --script=discovery`

# Wordlists (Kali Linux common locations)

- /usr/share/metasploit-framework/data/wordlists/common_users.txt
- /usr/share/metasploit-framework/data/wordlists/unix_passwords.txt 
- /usr/share/wordlists/rockyou.txt (gzip -d /usr/share/wordlists/rockyou.txt.gz)
- /usr/share/wordlists/metasploit/root_userpass.txt : use for ssh brute
- /usr/share/metasploit-framework/data/wordlists/common_passwords.txt
- /usr/share/commix/src/txt/usernames.txt 
- /usr/share/metasploit-framework/data/wordlists/unix_users.txt
- /usr/share/metasploit-framework/data/wordlists/directory.txt
- /usr/share/wordlists/dirb/common.txt
- /usr/share/metasploit-framework/data/wordlists/sensitive_files.txt
- /usr/share/webshells/asp/ - windows (iis)
- /usr/share/webshells/php/php-reverse-shell.php - linux (apache)
- /usr/share/windows-resources/binaries/


# Cheatsheets:

- https://rosettacode.org/wiki/Execute_a_system_command
- https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Reverse%20Shell%20Cheatsheet.md
- https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet
- https://pentestmonkey.net/category/tools/web-shells