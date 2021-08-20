altdns -i known-subdomains.txt -o raw-data_output -w words.txt -r -s results_output.txt

# Basic usage
./bin/massdns -r lists/resolvers.txt -t A domains.txt > results.txt
#In combination with dnsgen 
cat domains.txt | dnsgen -w words.txt -f - | massdns -r lists/resolvers.txt -t A -o S -w massdns.out

# dnsgen
dnsgen known-domains.txt


# Use other ports
cat domains.txt | httprobe -p http:81 -p https:8443
# Concurrency - You can set the concurrency level with the -c flag: 
cat domains.txt | httprobe -c 50

