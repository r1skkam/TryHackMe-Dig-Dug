# Dig Dug
```Turns out this machine is a DNS server - it's time to get your shovels out!```

[TryHackMe | Dig Dug](https://tryhackme.com/room/digdug)

[TryHackMe | DNS in detail](https://tryhackme.com/room/dnsindetail)

[TryHackMe | Passive Reconnaissance](https://tryhackme.com/room/passiverecon)

[TryHackMe | DNS Manipulation](https://tryhackme.com/room/dnsmanipulation)


```
root@ip-10-10-251-244:~# nslookup -type=a givemetheflag.com 10.10.232.40
Server:		10.10.232.40
Address:	10.10.232.40#53

givemetheflag.com	text = "flag{0767ccd06e79853318f25aeb*REDACTED*}"

root@ip-10-10-251-244:~# 
```
```
root@ip-10-10-251-244:~# dig @10.10.232.40 givemetheflag.com

; <<>> DiG 9.11.3-1ubuntu1.13-Ubuntu <<>> @10.10.232.40 givemetheflag.com
; (1 server found)
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 49712
;; flags: qr aa; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 0

;; QUESTION SECTION:
;givemetheflag.com.		IN	A

;; ANSWER SECTION:
givemetheflag.com.	0	IN	TXT	"flag{0767ccd06e79853318f25aeb*REDACTED*}"

;; Query time: 0 msec
;; SERVER: 10.10.232.40#53(10.10.232.40)
;; WHEN: Sat May 14 09:54:26 BST 2022
;; MSG SIZE  rcvd: 86
```
