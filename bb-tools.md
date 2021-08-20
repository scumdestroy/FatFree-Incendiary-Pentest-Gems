
# URLS
--------------------------------------------
galer : get urls/endpoints/links from URL
  > galer -u <list-or-url> -o <output> -c <int> -e <only-extension>  --in-scope 

gau -o <output> -p <proxy-url> -subs [include subs]

waybackurls -get-versions [check same URL at diff. dates]

p3 /root/bugbounty/urls/WayRobots/wayrobots.py -i <host> -o <out> -y <2c014-2019>

urlgrab --url <URL> --depth <666> --proxy <url> --threads <666> --delay <420> --random-agent

gal -t <url/domain>
---------------------------------------------------------
# HTCAP : dom/ajax request hunter , first - crawl
p2 /root/bugbounty/urls/htcap/htcap.py crawl http://satan.666 satan.db (creates a db)
# second : scan, i.e. run sqlmap x 10 concurrent like this (r: req types, n: threads, p: proxy):
htcap.py scan -r xhr -n 10 sqlmap satan.db
# util (report | lsvuln | lsajax)
htcap.py util report target.db target.html
htcap.py util lsvuln target.db
# chain cmds with '\;'
htcap.py crawl https://htcap.org htcap.db \; scan native \; scan sqlmap
---------------------------------------------------------------
# 403 bypass madness : 
403sum <URL>
----------------------------------------------------------
# Screenshot tools
>GOSTARE
go-stare -t <url or urls.txt>
subfinder -d <DOMAIN.com> -silent | httpx -silent | go-stare -o ./out
gau <DOMAIN.com> | go-stare -o ./out -q 50
>EYEWITNESS
eyewitness -f <urls.txt> --web
options: -x <nmap.xml> --resolve  --prepend-https (if just domains.com) --add-http-ports 8018,8088 --add-https-ports 9433 --only-ports 1488,666
> aquatone
cat urls.txt | aquatone -ports (small,medium,large,xlarge) -proxy <url> 
> RECONCAT
php /root/recon/reconcat/recon --url=https://github.com -t10 

> eyeballer - for large scopes, it analyzes your screenshots
eyeballer train
eyeballer.py --weights YOUR_WEIGHTS.h5 evaluate
eyeballer.py --weights YOUR_WEIGHTS.h5 predict YOUR_FILE.png
eyeballer.py --weights YOUR_WEIGHTS.h5 predict PATH_TO/YOUR_FILES/

----------------------------------------------------------
# RESOLVE SUBDOMAINS/ENDPOINTS
httprobe (-c 50 -p http:8888 -method PUT -prefer-https)
httpx/httpxxx
fff  (-m PUT  -o output -b <data>(body) -H <header> -d <delay-seconds>  [-S save responses] )
fprobe (-i urls.txt -c 100 -p http:8888 -prefer-https [-s skip 80,443] [-cidr <range> generate IPs]
urlprobe (-c 100 [-t 10 ratelimit])
# DNS STYLE RESOLVING
dnsx
dnsdig
dnsenum-(brute.sh, reverserange.sh, zonetransfer.sh,reverse.sh)
dnsmap/dnsmap-bulk
dnsrecon
dnsprobe
dns_shark
dnsub
dnswalk
# JANN-style DNS
dnssearch2hakrevdns
dnsgen2massdns
------------------------------------------
# PORTS
```
naabu
nmap
bash /root/bugbounty/ports/PortWitness/portwitness.sh <URL/domain.com>
p2 /root/bugbounty/ports/PortWitness/PortWitness_Python/PortWitness_Python.py <domain.com> 

```
# PORTSCAN.SH
-n:naabu+nmap, -m:masscan+nmap, -s:shodanfy, -p:simple-nmap
/root/bugbounty/ports/portscan.sh/portscan.sh -o <output-folder> -n <subs.txt> -p <subs.txt (same one)>

----------------------------------------------------------------------
# HOST HEADER INJECT
cat urls.txt | hinject -v

--------------------------------
# FINGERPRINT
webtech -u <URL>
