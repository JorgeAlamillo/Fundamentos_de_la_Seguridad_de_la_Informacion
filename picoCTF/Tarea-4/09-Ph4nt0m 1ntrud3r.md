### Ph4nt0m 1ntrud3r

### Descripción

A digital ghost has breached my defenses, and my sensitive data has been stolen! 😱💻 Your mission is to uncover how this phantom intruder infiltrated my system and retrieve the hidden flag.To solve this challenge, you'll need to analyze the provided PCAP file and track down the attack method. The attacker has cleverly concealed his moves in well timely manner. Dive into the network traffic, apply the right filters and show off your forensic prowess and unmask the digital intruder!Find the PCAP file here [Network Traffic PCAP file](https://challenge-files.picoctf.net/c_verbal_sleep/586d0206891cc683bae1160ad6b0e05d7e10e7b2df122c0441ab06581038dd32/myNetworkTraffic.pcap) and try to get the flag.
### Solución


┌──(JorgeMSI㉿MSI)-[~/phantom]
└─$ wget -q https://challenge-files.picoctf.net/c_verbal_sleep/586d0206891cc683bae1160ad6b0e05d7e10e7b2df122c0441ab06581038dd32/myNetworkTraffic.pcap

┌──(JorgeMSI㉿MSI)-[~/phantom]
└─$ ls
myNetworkTraffic.pcap

┌──(JorgeMSI㉿MSI)-[~/phantom]
└─$ tshark -r myNetworkTraffic.pcap -Y "tcp" -T fields -e tcp.segment_data | xxd -p -r | base64 -d
Command 'tshark' not found, but can be installed with:
sudo apt install tshark

┌──(JorgeMSI㉿MSI)-[~/phantom]
└─$ sudo apt install tshark

┌──(JorgeMSI㉿MSI)-[~/phantom]
└─$ tshark -r myNetworkTraffic.pcap -Y "tcp.len > 0" -T fields -e frame.time_epoch -e tcp.segment_data | sort -n | awk '{print $2}' | xxd -p -r | base64 -d
Warning: program compiled against libxml 215 using older 214
�Ѓ]B?Z��picoCTF{1t_w4snt_th4t_34sy_tbh_4r_2e1ff063}�i�

picoCTF{1t_w4snt_th4t_34sy_tbh_4r_2e1ff063}
### Notas
### Referencias