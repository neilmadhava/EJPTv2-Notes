# Information Gathering and Enumeration Modules

- in nmap, export scan output in xml format with -oX flag.
- in msfconsole, db_import <file> (the previously exported file)
- hosts, services, loot, creds, notes (common commands in metasploit)

Port scanning with bash script
```bash
#!/bin/bash
for port in {1..1000}; do
	timeout 1 bash -c "echo >/dev/tcp/$1/$port" 2>/dev/null && echo "port $port is open"
done
```

## Modules:
### Port Scanning

- auxiliary/scanner/portscan/tcp

### FTP

- auxiliary/scanner/ftp/ftp_login : brute force ftp
- auxiliary/scanner/ftp/anonymous : anonymous login test

### SMB

- auxiliary/scanner/smb/smb_version - exact version of smb
- auxiliary/scanner/smb/smb2 - smb2 protocol supported?
- auxiliary/scanner/smb/smb_enumusers
- auxiliary/scanner/smb/smb_enumshares
- auxiliary/scanner/smb/pipe_auditor : determine what named pipes are accessible over SMB  (req creds)
- auxiliary/scanner/smb/smb_login
- exploit/windows/smb/psexec
- auxiliary/scanner/smb/smb_ms17_010 - eternalblue vuln tester

### HTTP

- auxiliary/scanner/http/apache_userdir_enum : find users on apache server
- auxiliary/scanner/http/brute_dirs : find intersting dirs
- auxiliary/scanner/http/dir_scanner : find interesting dirs
- auxiliary/scanner/http/dir_listing : test directory listing vuln
- auxiliary/scanner/http/http_put : upload/delete file to/from server
- auxiliary/scanner/http/files_dir : finds interesting files in a dir
- auxiliary/scanner/http/http_login : brute force http login
- auxiliary/scanner/http/http_header : get header of a path
- auxiliary/scanner/http/http_version : get http server version
- auxiliary/scanner/http/robots_txt : get robots.txt file

### MySQL

- auxiliary/admin/mysql/mysql_enum : various enums on mysql server
- auxiliary/admin/mysql/mysql_sql : send sql query to server
- auxiliary/scanner/mysql/mysql_file_enum : Enumerate files and directories using the MySQL load_file feature
- auxiliary/scanner/mysql/mysql_hashdump : dump hashes of mysql user
- auxiliary/scanner/mysql/mysql_login : brute force mysql auth
- auxiliary/scanner/mysql/mysql_schemadump : get structure of db, table etc
- auxiliary/scanner/mysql/mysql_version : get mysql version
- auxiliary/scanner/mysql/mysql_writable_dirs : get writeable dirs

### SSH

- auxiliary/scanner/ssh/ssh_version
- auxiliary/scanner/ssh/ssh_login

### SMTP

- auxiliary/scanner/smtp/smtp_enum

## Wordlists

- /usr/share/metasploit-framework/data/wordlists/directory.txt
- /usr/share/metasploit-framework/data/wordlists/common_users.txt
- /usr/share/metasploit-framework/data/wordlists/common_passwords.txt
- /usr/share/commix/src/txt/usernames.txt 
- /usr/share/metasploit-framework/data/wordlists/unix_users.txt