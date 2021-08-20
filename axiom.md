# start
axiom init
axiom-boxes get pry0cc/lazy
axiom-ssh <droplet>
# Scan and kill
axiom-select 'fleet' (should already be selected tho)
axiom-scan <input> -m <module> -o <text outfile> <any other args>
axiom-scan subs.txt -m httpx -o http.txt
axiom-scan http.txt -m nuclei -o nuclei.txt
axiom-scan http.txt -m gowitness -o screenshots 
axiom-scan subs.txt -m dnsprobe -o dns.txt 
axiom-scan ips.txt -m nmap -oG portscan.txt
axiom-scan ips.txt -m nmap -oX full -p- -T5 -sV --script=vulners 
axiom-scan ips.txt -m masscan -oG masscan.txt


# Scanning with the fleet
axiom-fleet scanners -i=15 -t=5
 axiom-scan "scanners*" -p443 -iL=targets.txt -m nmapx -sV -C -PN
## copy files 
axiom-scp testy01:~/path/to/file output/test.txt 
# copy file from testy01:~/path/to/file to output/test.txt
axiom-scp 'testy*':~/path/to/file 'output/$name.txt' 
# Copy a file from every single instance in the testy fleet from the path to the name of the instance, $name gets interpolated. 
axiom-scp test.txt 'testy*':/path/to/file 
#  Copy test.txt to the same path on each fleet

# proxy
```
axiom-proxy '<fleet>*' or instance or '*name*'
```
# TELL A BUNCH OF GUYS TO DO A THING
axiom-exec <cmd> <instance>
axiom-exec 'nmap -T5 navisec.io' 'testy01' -q --cache 
axiom-execb 'nmap -T5 navisec.io' 'testy01' -q --cache
