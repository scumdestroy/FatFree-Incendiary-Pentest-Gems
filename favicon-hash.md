
# calculate favicon hashes
```
curl -s -L -k https://gitlab.com/favicon.ico | python3 -c 'import mmh3,sys,codecs; print(mmh3.hash(codecs.encode(sys.stdin.buffer.read(),"base64")))'
```

#then do shodan search on the hash

```
shodan search http.favicon.hash:1278323681
```
