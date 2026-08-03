## Objective
The objective of this lab is to generate and analyze live attack traffic to understand reconnaissance and brute-force patterns at the network layer with ```WIRESHARK```

## Environment


|   Role   |   Machine    | Details |
| -------- | -------- | -------- |
|  Attacker | Kali Linux  | host my hydra, Nmap |
| Server / Client | Ubuntu OS |  SSH server created,  with Wireshark listening and generating Packet capture to detect brute-force & Nmap recon attempt |
| Network | VM-ware internal network (Host-only) |  Isolated lab environment |

## Steps Taken
1. Setup Wireshark on ubuntu, start wireshark, generate & forward pcap logs  - sudo tcpdump -i ens33 -w /home/$USER/lab_capture.pcap port 22
2. run an Nmap scan on Kali against the Ubuntu OS IP - nmap -sV -P- 192.168.142.139
3. run hydra brute-force against the SSH user created in ubuntu OS - hydra -l hrstaff1 -P wordlist.txt ssh://192.168.142.138

## Analysis
Reconnaissance detection: 







| Header 1 | Header 2 | Header 3 |
| -------- | -------- | -------- |
| Row 1 A  | Row 1 B  | Row 1 C  |
| Row 2 A  | Row 2 B  | Row 2 C  |
