# Metasploit Modules

- auxiliary/scanner/smb/smb_login - get login creds
- exploit/windows/smb/psexec (can be used to pass NTLM hashes as password)
	- use login creds from step before
	- can work with ntlm hashes too (use lt:ntlm hash as smbpass - set target command / native upload)
	
	![psexec output](./images/smb-01.png)

# EternalBlue:

- MS17-010/CVE-2017-0144
- takes advantage of vulnerability in SMBv1 protocol
- attackers send malicious packets that facilitate arbitrary command exec
- used in WannaCry ransomware attack
- gives elevated privs by default
- https://github.com/3ndG4me/AutoBlue-MS17-010
- affects Vista, Win7, WinServ2008, Win8.1, WinServ2012, Win10, WinServ2016
- nmap script
	- smb-vuln-ms17-010
- exploit/windows/smb/ms17_010_eternalblue