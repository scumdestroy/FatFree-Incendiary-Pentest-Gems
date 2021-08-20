## DOCKER FUCKER ##

to enumeate the container you are in:
```
for i in {1..254}; do (ping -c 1 172.19.0.$i | grep "bytes from" | cut -d':' -f1 | cut -d' ' -f4 &); done
```

