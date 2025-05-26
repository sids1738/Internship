Task 1: Scan Your Local Network for Open Ports

Objective
Learn basic network reconnaissance by identifying open ports on devices within your local network.

---------

Tools Used
- Nmap (network scanner)
- Wireshark (network packet analyzer)
- Kali Linux via WSL2

---------

 Steps Performed

1. Installed Nmap

sudo apt install nmap 

2. Ran Nmap SYN Scan

nmap -sS 172.28.13.0/24 -oN scan_results.txt
My IP range was (172.28.13.0/24) found it using ifconfig

3. Installed Wireshark

sudo apt install wireshark 

4.Added permissions using-

sudo usermod -aG wireshark $USER

Restarted WSL session to apply group changes.

5. Captured Network Traffic with Wireshark
Started Wireshark, selected Ethernet interface, and captured packets during the Nmap scan.

---------

Analysis-

Nmap scan analysis-

-Open port 5901 indicates a VNC service is running on the detected host.
-VNC may pose risks if not secured with encryption and strong credentials.

Wireshark Analysis-

-Broadcasts from 172.28.0.1 suggest local device/service discovery.
-DNS lookups for services.addons.mozilla.org confirm browser (likely Firefox) activity.
-VNC port activity (5901) matched Nmap findings.
