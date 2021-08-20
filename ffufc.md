# You should usually use -mc all -ac, it will catch 99% of crap noise but...
401 or 403 - if whole host is this then nvm but if you get  few - try to bypass via path traversal or verb tampering.  If -ac don't catch it its prob a (misconfigured) rule in ACL 

301 - usually mean directories. next best after 200s

# USUAL TRASH BUT MAYBE
302 - almost always trash
400 + 404 : if you see them and have -ac its interesting, because they're a diff size, check into it
429 - you are rate limited so stop
500 - sometimes weird fuzz payload makes it pop but sometimes interesting - do param brute force here
502, 504 - usually weak server or too much traffic but maybe once in a  while...
