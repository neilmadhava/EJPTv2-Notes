# Active Information Gathering

- nmap
- netdiscover
	- `sudo netdiscover -i eth0 -r 192.168.2.0/24`
- For doing DNS zonetransfer: `dig axfr <nameserver> domain`
	- `dig axfr @nsztm1.digi.ninja zonetransfer.me`
- `fierce -dns zonetransfer.me`