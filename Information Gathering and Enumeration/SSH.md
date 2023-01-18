# Banner grabbing

- `nc <ip> 22`
- `ssh root@<ip>`

# Nmap scripts

- ssh2-enum-algos : enum encryption_algos supported by ssh server
- ssh-hostkey --script-args ssh_hostkey=full
- ssh-auth-methods --script-args="ssh.user=student" : check none_auth
- ssh-run --script-args="ssh-run.cmd=cat /home/student/FLAG,ssh-run.username=student,ssh-run.password="
- ssh-brute --script-args userdb=/root/users

# Hydra

- `hydra -l <user> -P <passlist> 192.40.231.3 ssh`

# Metasploit Modules

- auxiliary/scanner/ssh/ssh_version
- auxiliary/scanner/ssh/ssh_login