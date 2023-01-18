# Vulnerability Scanning

## db_autopwn

- https://github.com/hahwul/metasploit-autopwn : plugin to auto detect vulns
- works if services and hosts are there in msf db

![move plugin to msf folder](./images/infoenum-01.png)
![load db_autopwn](./images/infoenum-02.png)
![db_autopwn output](./images/infoenum-03.png)
- db_autopwn -p -t -PI 445
- analyze

![db_autopwn analyze output](./images/infoenum-04.png)


## wmap plugin

- load wmap
- wmap_sites -a 192.157.89.3 : add site
- wmap_targets -t http://192.157.89.3 : add target ip address
- wmap_sites -l
- wmap_targets -l
- wmap_run -t : display list of available modules that can be run
- wmap_run -e : run enabled modules