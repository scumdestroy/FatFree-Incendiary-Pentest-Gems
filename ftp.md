## BANNER GRAB
telnet -vn IPADDR 21

# anon login obviously
# try with browser ftp://10.10.10.10:21

#download all files
wget -m ftp://anonymous:anonymous@10.10.10.98 
wget -m --no-passive ftp://anonymous:anonymous@10.10.10.98 

#COMMANDS
USER username
PASS password
PORT 127,0,0,1,0,80 (will connect to 127.0.0.1:80, you need to put 5th char as '0' and the 6th as the port in decimal)
LIST
STOR /path/idktxt - store data from passive connection or from PORT to a file
RETR /path/file - after connection, it wll send the file thru that connection
TYPE i - set transfer to binary
PASV - opena passive connection

##CONFIG FILES
ftpusers
ftp.conf
proftpd.conf

