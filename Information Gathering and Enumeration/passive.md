# Passive Information Gathering

## Website Recon

- host <website> : dns lookup - to get pub ip of website and email servers
- robots.txt / sitemap.xml (look for hidden files)
- whatweb <website> : tech used
- httrack : used to download website source
- whois
- netcraft.com - https://sitereport.netcraft.com
- dnsrecon -d hackersploit.org : dns recon, get records for domain
- dnsdumpster.com
- wafw00f <website> like wafw00f betsol.com -a : get app firewall
- sublist3r -d betsol.com -e google,yahoo vc
- googledork: site,filetype,inurl,intitle,cache 
	- https://www.exploit-db.com/google-hacking-database
- waybackmachine
- /theHarvester.py -d betsol.com -b google,linkedin : email harvester
- dnsenum betsol.com : can be used for zonetransfer