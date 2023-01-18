# Nmap

- `nmap --top-ports 7000 <ip>` : default port scan doesn't show
- port 5985

# Metasploit

- auxiliary/scanner/winrm/winrm_login : brute force
- IMPORTANT: use auxiliary/scanner/winrm/winrm_auth_methods
	- need to use a valid auth method while connecting to service
	- https://docs.microsoft.com/en-us/windows/win32/winrm/authentication-for-remote-connections
	  
	  ![winrm_auth_methods output](./images/winrm-01.png)
	  
- auxiliary/scanner/winrm/winrm_cmd : execute cmd on target server as legit user - need creds
- exploit/windows/winrm/winrm_script_exec: interactive meterpreter session
	- set FORCE_VBS true

# References

https://www.rapid7.com/db/modules/auxiliary/scanner/winrm/winrm_login
https://www.rapid7.com/db/modules/auxiliary/scanner/winrm/winrm_auth_methods
https://www.rapid7.com/db/modules/auxiliary/scanner/winrm/winrm_cmd
https://www.rapid7.com/db/modules/exploit/windows/winrm/winrm_script_exec
