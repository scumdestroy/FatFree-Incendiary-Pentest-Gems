## METHODS
http METHOD example.org
# automatic POST i.e.
http example.org param=hell
# localhost requests
http :3000 or http :/gang

#headers with :
Referer:http://url.com User-Agent:satan/6.66
# url parameters appended to URI with '=='
devils==cool
# use -f for forms or -j for json data and then '='
-j skin=white race=best
# walrus for non-string JSON data fields (and you need -j)
admin:=true devil:=666
#form fields with "@"
cv@'~/Documents/CV.pdf;type=application/pdf'
# data field but takes a file path and embeds content '=@'
essay=@Documents/essay.txt
# above but with JSON ':=@'
package:=@./package.json
---
# DATA TYPES 
-f form
-j json
--multipart
--boundary
---
compress with -x
---
# STYLE
--pretty (all, colors, format)
-s autumn, igor, monokai, xcode, trac, tango, stata
---
# print
-h headers only
-b body only
-v verbose
--all
---
# SAVED SESSIONS
-d download, filename is automatic unless -d <file>
-c continue (needs --output as well)
--session <SESSION NAME OR PATH> - will retain custom headers, auth creds and cookies
---
--auth USER[:PASS], -a USER[:PASS]
--proxy PROTOCOL:PROXY_URL
--follow, -F
--check-status
---
# FOR LFI AND 403 BYPASSES
--path-as-is (don't squash /../ and /./)
---
# SSL
--verify (default is yes, change it to no or false)
--ssl {ssl2.3,tls1,tls1.1,tls1.2}
 --ciphers CIPHERS
--cert CERT
--cert-key CERT_KEY

