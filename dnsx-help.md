# Remove dead records
subfinder -silent -d hackerone.com | dnsx

#get A records
subfinder -silent -d hackerone.com | dnsx -silent -a -resp

#CNAMES
subfinder -silent -d hackerone.com | dnsx -silent -cname -resp

#Via PTR Query
mapcidr -cidr 173.0.84.0/24 -silent | dnsx -silent -resp-only -ptr

#Remove wildcards
dnsx -l airbnb-subs.txt -wd airbnb.com -o output.txt

-t : threads (default 250)
-aaaa : AAAA record
-mx : MX record
-ns : NS record
-soa : SOA record
-txt : TXT record
