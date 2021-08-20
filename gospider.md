## PUT THE DOMAIN OR URLS.txt AT THE END
## crawl one domain w/ burp proxy
gospider -p http://127.0.0.1:8080 -t 5 -d 0 --sitemap --include-subs -r -a -s 

## crawl a list of urls/domains w/ burp proxy
gospider -p http://127.0.0.1:8080 -t 5 -d 0 --sitemap --include-subs -r -a -S 

## one domain no proxy
gospider -p http://127.0.0.1:8080 -t 5 -d 0 --sitemap --include-subs -r -a -s 

## crawl a list of urls/domains w/ burp proxy
gospider -p http://127.0.0.1:8080 -t 5 -d 0 --sitemap --include-subs -r -a -S
