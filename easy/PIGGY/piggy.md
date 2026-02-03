# Piggy Lab Report

- Q1) PCAP One) What remote IP address was used to transfer data over SSH? (Format: X.X.X.X)
  - Either going to Statistics and seeing which IP is working with port 22 or searching for ssh in the display filter will reveal the IP address used to transfer data over ssh

- Q2) PCAP One) How much data was transferred in total? (Format: XXXX M)
  - Seeing the bytes column next to the IP address shows how much data was transferred in total

- Q3) PCAP Two) Review the IPs the infected system has communicated with. Perform OSINT searches to identify the malware family tied to this infrastructure (Format: MalwareName)
  - Running all IP addresses on virustotal, one IP comes out infected where it is being used for hosting and botnet CNS panel for the trickbot malware

- Q4) PCAP Three) Review the two IPs that are communicating on an unusual port. What are the two ASN numbers these IPs belong to? (Format: ASN, ASN)
  - Reviewing statistics tab and then conversations, under TCP it will show the unusual post where the communication is taking place

- Q5) PCAP Three) Perform OSINT checks. What malware category have these IPs been attributed to historically? (Format: MalwareType)
  - Virustotal scan shows the destination IP has been connected to C2 malware

- Q6) PCAP Three) What ATT&CK technique is most closely related to this activity? (Format: TXXXX)
  - MITRE ATT&CK framework shows resource hijacking 

- Q7) PCAP Four) Go to View > Time Display Format > Seconds Since Beginning of Capture. How long into the capture was the first TXT record query made? (Use the default time, which is seconds since the packet capture started) (Format: X.xxxxxx)
  - Using the command dns.qry.type == 16 will filter packets as per the txt query type and the first query will show how long into the capture was the first txt record query made

- Q8) PCAP Four) Go to View > Time Display Format > UTC Date and Time of Day. What is the date and timestamp? (Format: YYYY-MM-DD HH:MM:SS)
  - Just change the time display format to UTC date and time of day to see the date and timestamp

- Q9) PCAP Four) What is the ATT&CK subtechnique relating to this activity? (Format: TXXXX.xxx)
  - Performing OSINT reveals the Mitre ATT&CK subtechnique relating to this activity
