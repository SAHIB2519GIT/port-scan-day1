\# 🔍 **Day 1 Port Scanning – Network Reconnaissance**



\*\*Author:\*\* Sahibjot Singh  

\*\*Date:\*\* 2025-09-22  

\*\*Tools:\*\* Nmap, Terminal / Command Prompt  

\*\*Purpose:\*\* Learn network scanning basics and gather information about hosts and services.



**Objective**

The goal of this exercise was to \*\*perform hands-on network reconnaissance\*\*, identify open ports, detect services, and document findings. This lays the foundation for practical cybersecurity skills.



 **Step 1: Discover My Network Info**



Command:

ip addr show



What I did:

Checked active network interfaces

Found my IPv4 address, subnet, and MAC address

Identified the interface to scan



Why it matters:

Knowing your network range ensures accurate scanning and prevents scanning the wrong interfaces.



&nbsp;**Step 2: Basic TCP SYN Scan**

Command:

nmap -sS -oA outputs/tcp\_syn  10.91.10.229



What I did:

Ran a TCP SYN scan to detect open ports

Saved outputs in .nmap, .xml, and .gnmap formats

Observed which services responded



Why it matters:

SYN scan is stealthy and fast, helping identify potential attack surfaces without fully connecting.



**Step 3: Service \& Version Detection**

Command:

nmap -sS -sV -oA outputs/service\_version 10.91.10.229



What I did:

Detected services running on each port

Gathered version info for security assessment

Sample Observations:



Why it matters:

Service versions help identify vulnerable software and plan further security analysis.



 **Step 4: OS Detection**

Command:

nmap -O -oA outputs/os\_detection  10.91.10.229



What I did:

Determined the operating systems of hosts

Recorded uptime and device types



Why it matters:

OS information is critical for identifying OS-specific vulnerabilities and planning further tests.



&nbsp;**Step 5: NSE Script Scan**

Command:

nmap -sS -sV --script=default -oA outputs/nse\_scan  10.91.10.229



What I did:

Ran Nmap Script Engine (NSE) with default scripts

Collected additional info such as HTTP headers, SSL details, and service fingerprints



Why it matters:

NSE scripts provide deeper insights into potential vulnerabilities and misconfigurations.



**Observations \& Lessons Learned**

TCP SYN scan is fast and stealthy

Service version detection reveals precise software information

OS detection adds context for exploitability

NSE scripts give insights into service misconfigurations

Learned to organize outputs professionally for analysis and reporting

Noted initial scanning challenges and how I resolved them



**Conclusion**

Day 1 of network reconnaissance provided hands-on experience in scanning networks, understanding open ports, detecting services, and documenting results.

Next steps: Explore advanced NSE scripts, vulnerability scanning, and Wireshark traffic analysis for deeper understanding.

