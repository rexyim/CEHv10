---


---

<h1 id="ceh-tools">CEH Tools</h1>
<h3 id="usniffersu"><u>Sniffers</u></h3>
<p><strong>Wireshark</strong>: The most popular packet sniffer with cross platform support.</p>
<p><strong>Tcpdump</strong>: A popular CLI sniffer available for both the Unix and Linux platforms.</p>
<blockquote>
<p>tcpdump -i eth0 # Capture on eth0</p>
</blockquote>
<p>tcpdump -w cap.log # Write to cap.log</p>
<p>tcpdump -r cap.log # Read from cap.log</p>
<p><strong>Windump</strong>: Windows version of tcpdump.</p>
<p><strong>Cain &amp; Abel</strong>: Its an all-in-one tool to capture packets and record passwords being used in a</p>
<p>MiTM. It can create an ARP and DNS poisoning events and the cracker works with methods</p>
<p>such as network packet sniffing, dictionary, brute force and cryptanalysis such as rainbow</p>
<p>attacks.</p>
<p><strong>Kismet</strong>: Wireless sniffing tool used to locate and discover hidden SSID’s. It can be used to</p>
<p>passively sniff the traffic and gain the password that way.</p>
<p><strong>Ntop</strong>: High speed web based traffic analysis.</p>
<p><strong>Network Miner</strong>: Packet sniffer, with built in OS finger printer. Drop down navigator for</p>
<p>filtering specific traffic. Automatically extracts files for packet capture; it will also extract</p>
<p>images. It will also pull some credentials for specific sites. It can also filter out “keywords” to</p>
<p>allow for filtering of specific information being sent across the network.</p>
<h3 id="uscannersu"><u>Scanners</u></h3>
<p><strong>Nmap</strong>: uses raw IP packets in novel ways to determine what hosts are available on the</p>
<p>network, what services (application name and version) those hosts are offering, what</p>
<p>operating systems (and OS versions) they are running, what type of packet filters/firewalls are</p>
<p>in use, and dozens of other characteristics.</p>
<blockquote>
<p>nmap -T4 -n -sS 192.168.0.1/24 # SYN</p>
</blockquote>
<p>Study -sT (tcp), -sS (syn), -sA (ack), -sF (fin), -sN (null), -sX (xmas), -sI (idle), -sU (udp), -sV (service detection), -O (OS detection)</p>
<p><strong>-sA</strong>: ACK Filtered/Unfiltered For detecting firewall, unfiltered (open/close) returns RST packet</p>
<p><strong>-sF</strong>: FIN Closed/Open|Filtered RST when closed, no response when open|filtered</p>
<p><strong>-sX</strong>: XMAS FIN, PSH, URG Same as FIN</p>
<p><strong>-sN</strong>: NULL Same as FIN</p>
<p><strong>-sU</strong>: UDP Open/Closed/Filtered/Open|Filtered UDP response when open, ICMP type 3 code 3 (Port Unreachable) when closed, other ICMP when filtered, no response when open|filtered</p>
<p><strong>-sI</strong>: <a>host:port</a>: IDLE Stealth scan using zombie host and IP fragmentation ID</p>
<p><strong>Zenmap</strong>: Nmap with a GUI and ability to plot a map for reference.</p>
<p><strong>Angry IP Scanner</strong>: (or simply ipscan) is an open-source and cross-platform network scanner</p>
<p>designed to be fast and simple to use. It scans IP addresses and ports as well as has many</p>
<p>other features.</p>
<p><strong>hping2 &amp; 3</strong>: Custom packet-crafting tool that can be used to precisely package packets to</p>
<p>scan and penetrate networks and bypass known security features.</p>
<blockquote>
<p>hping3 -c 3 --scan 1-3000 -S -V 192.168.1.254 # Scans port 1-3000 on 192.168.1.254 with 3 SYN packets each</p>
</blockquote>
<p>hping3 -c 100 -d 120 -S -p 21 --flood --rand-source <a href="http://google.com">google.com</a> # Flood google with 100 counts, SYN packets with data size 120 bytes, on port 21, with random spoofed IP source</p>
<p><strong>SuperScan</strong>: allows you to quickly scan a range of IP addresses and do TCP port scanning. It</p>
<p>can check all ports, or the ones you select. It is a very fast and powerful tool. Supports</p>
<p>banner grabbing, ping, whois, tracert. Recently bought by McAfee.</p>
<p><strong>Zanti (mobile)</strong>: An Android software used to Scan Ports, MiTM, Session Hijack, Redirect URL</p>
<p>traffic, used for Pentesting with a noble device.</p>
<p><strong>NBTScan</strong>: It sends a NetBIOS status query to each address in a supplied range and lists</p>
<p>received information in human readable form. For each responded host it lists IP address,</p>
<p>NetBIOS computer name, logged-in user name and MAC address. <strong>SUPER FAST SCANS</strong></p>
<p><strong>NetScan Tools</strong>: Created in 1999 to automate the plethora of internet tools to work with one</p>
<p>GUI supported by Windows platforms. OS Fingerprinting, Packet sniffing, port scanning,</p>
<p>packet flooding, mail exchange validation.</p>
<p><strong>Nessus</strong>: Vulnerability scanner that is used by pentesters, hackers, and enterprise security</p>
<p>engineers.</p>
<h3 id="uenumerationu"><u>Enumeration</u></h3>
<p><strong>DumpSec</strong>: Reveals users, groups, printers, shares, registry info in an easy to digest human</p>
<p>readable format from a targeted system. Very useful for finding out intimate information</p>
<p>about the specific system for privilege escalation purposes.</p>
<p><strong>SuperScan</strong>: Also used for enumeration. *See Scanning</p>
<p><strong>Netcat</strong>: A simple tool that can read and write data across a TCP or UDP connection. It’s very</p>
<p>useful because it can create almost any type of connection. Including session binding. It</p>
<p>allows actors to create shell and reverse shell connections between two endpoint. Allowing</p>
<p>them to send / receive files and execute commands on both the host and compromised</p>
<p>systems. It has since lost support; consequently the Nmap project has incorporated an</p>
<p>upgraded version called Ncat. Other remakes: Socat, OpenBSD’s nc, Cryptcat, netcat6,</p>
<p>pnetcat, etc.</p>
<blockquote>
<p>nc -zv -w 1 <a href="http://google.com">google.com</a> 21 # Scan google’s port 21, -z scan, -v verbose, -w timeout</p>
</blockquote>
<p>nc -lvp 6969 # Opens a server on 6969, -l listens, -v verbose, -p port 6969</p>
<p>nc 192.168.1.54 6969 # Banner Grab with GET / HTTP/1.1 after connecting</p>
<p><strong>CRYPTCAT</strong>, netcat alternative with encryption involved</p>
<p><strong>Cryptcat</strong>: A variant of netcat that encrypts communication; making it useful to evade the</p>
<p>detection of IDS or traffic sniffing.</p>
<p><strong>TCPView</strong>: It will enumerate all TCP and UDP connections on the end point running the</p>
<p>application. Will resolve domain names for the IP’s connected to the system. Monitors</p>
<p>changing connections and can close existing connections.</p>
<p><strong>Sysinternals Suite</strong>: A suite of sysinternal tools made by Microsoft for troubleshooting.</p>
<p>NirSoft Suite: A suite of tools used to automate the troubleshooting of Windows.</p>
<p><strong>Firewalk</strong>: An active reconnaissance network security tool that attempts to determine what layer 4 protocols a given IP forwarding device will pass. It works by sending out TCP or UDP packets with a TTL one greater than the targeted gateway.</p>
<blockquote>
<p>firewalk -S1-1000 -i eth0 -n -pTCP 192.168.1.254 192.168.1.30 # Scan port 1-1000 through eth0, no hostname resolution, with TCP protocol, via gateway 192.168.1.254 against target 192.168.1.30</p>
</blockquote>
<p><strong>nslookup</strong>: A network administration command-line tool available in many computer operating systems for querying the Domain Name System to obtain domain name or IP address mapping, or other DNS records.</p>
<blockquote>
<p>nslookup</p>
</blockquote>
<blockquote>
<blockquote>
<p>server <a href="http://ns1.google.com">ns1.google.com</a></p>
</blockquote>
</blockquote>
<p>set type=any # Or A (address), NS (nameserver), MX (mailserver), SOA (start of authority), CNAME (canonical name), PTR (pointer)</p>
<p>ls -d <a href="http://google.com">google.com</a> # Zone transfer</p>
<p><strong>DIG</strong>: A network administration command-line tool for querying the Domain Name System. dig is useful for network troubleshooting and for educational purposes. It can operate based on command line option and flag arguments, or in batch mode by reading requests from an operating system file.</p>
<blockquote>
<p>dig <a href="http://www.google.com">www.google.com</a></p>
</blockquote>
<p>dig mx <a href="http://www.google.com">www.google.com</a> # Get mail server entries</p>
<p>dig axfr @ns1.google.com <a href="http://www.google.com">www.google.com</a> # Zone transfer</p>
<p><strong>NBTSTAT</strong>: A diagnostic tool for NetBIOS over TCP/IP. It is included in several versions of Microsoft Windows. Its primary design is to help troubleshoot NetBIOS name resolution problems.</p>
<blockquote>
<p>nbtstat -A 192.168.1.254 # Get remote NetBIOS table</p>
</blockquote>
<p>nbtstat -n # Get local table</p>
<p><strong>WHOIS</strong>: Searches for an object in a WHOIS database. WHOIS is a query and response protocol that is widely used for querying databases that store the registered users of an Internet resource, such as a domain name or an IP address block, but is also used for a wider range of other information.</p>
<blockquote>
<p>whois <a href="http://google.com">google.com</a></p>
</blockquote>
<p>Important WHOIS Registrars:</p>
<p><strong>ARIN</strong> - North America</p>
<p><strong>APNIC</strong> - Asia Pacific</p>
<p><strong>AFRINIC</strong> - Africa</p>
<p><strong>LACNIC</strong> - Latin America and Caribbean</p>
<p><strong>RIPE</strong> - Europe</p>
<p><strong>Maltego</strong>: An interactive data mining tool that renders directed graphs for link analysis. The tool is used in online investigations for finding relationships between pieces of information from various sources located on the Internet.</p>
<p><strong>sc query</strong>: Obtains and displays information about the specified service, driver, type of service, or type of driver.</p>
<pre><code>
sc [&lt;ServerName&gt;] query [&lt;ServiceName&gt;] [type= {driver | service | all}] [type= {own | share | interact | kernel | filesys | rec | adapt}] [state= {active | inactive | all}] [bufsize= &lt;BufferSize&gt;] [ri= &lt;ResumeIndex&gt;] [group= &lt;GroupName&gt;]

</code></pre>
<h3 id="upassword-cracking-toolsu"><u>Password Cracking Tools</u></h3>
<p><strong>L0phtCrack</strong>: A password cracking application used for locally or remotely locating user</p>
<p>account information and cracking the corresponding passwords. Windows/Unix/Linux/</p>
<p>FreeBSD/ etc. Can be used for periodically scanning and cracking system passwords.</p>
<p><strong>Ophcrack</strong>: Free version of Ophcrack. Less features. Not as robust.</p>
<p><strong>John the Ripper</strong>: CLI password cracking utility that can have custom rules created as well as</p>
<p>use custom password lists to crack passwords.</p>
<blockquote>
<p>john shadow.txt</p>
</blockquote>
<p>john --wordlist=passwords.txt shadow.txt</p>
<p><strong>Trinity Rescue Kit</strong>: Live Linux distribution that aims specifically at recovery and repair</p>
<p>operations on Windows machines, but is equally usable for Linux recovery issues. Since</p>
<p>version 3.4 it has an easy to use scrollable text menu that allows anyone who masters a</p>
<p>keyboard and some English to perform maintenance and repair on a computer, ranging from</p>
<p>password resetting over disk cleanup to virus scanning.</p>
<p><strong>Medusa</strong>: Remote, speedy, modular brute force cracker for network services. HTTP, MySQL,</p>
<p>SMB, SMTP, SNMP, SSHv2</p>
<p><strong>RainbowCrack</strong>: Cracks hashes referenced against rainbow tables. It’s different from</p>
<p>traditional brute force crackers in that it uses large pre-computed tables called “rainbow</p>
<p>tables”; which reduces the amount of time the brute force takes.</p>
<p><strong>Brutus</strong>: Older remote password cracker.</p>
<h3 id="uwireless-toolsu"><u>Wireless Tools</u></h3>
<p><strong>Kismet</strong>: A sniffing tools and also a multi-purpose wireless tool. It can be used for IDS and</p>
<p>many other things.</p>
<p><strong>inSSIDer</strong>: Used to monitor local WiFi traffic and identify the channels different networks are</p>
<p>communicating on. It was originally designed for optimizing Office / Home network WAP</p>
<p>placement to reduce interference and produce the most optimal signals for the environment.</p>
<p><strong>Reaver</strong>: WPS brute forcing tool. This tool waits to intercept the WPS beacon; once it’s</p>
<p>captured it will brute force the WPS PIN and the PSK password.</p>
<p><strong>Netstumbler (Old but useful on 32bit systems)</strong>: Similar to inSSIDer, but not as feature rich.</p>
<p><strong>Bluesnarfer</strong>: A tool used to steal information from a mobile device through the bluetooth</p>
<p>connection.</p>
<p><strong>Aircrack-ng</strong>: Is a tool suite used to assess WiFi security. It focuses on monitoring, attacking,</p>
<p>testing and cracking a WAP. It can capture and analyze packets; create replay attacks,</p>
<p>deauthentication with injection techniques; test WiFi cards and their driver capabilities; and</p>
<p>crack WEP and WPA PSK (1 and 2). It can also conduct fragmentation attacks.</p>
<p><img src="/images/wireless_aircrack-ng.png" alt="Aircrack-ng Suite"></p>
<p><strong>Airmon-ng (Aircrack)</strong>: Aircrack’s sniffing tool.</p>
<p><strong>Airodump-ng (Aircrack)</strong>: Used to capture 802.11 packets, especially good at capturing WEP</p>
<p>IV’s to be used with Aircrack-ng. It can also be used to log the GPS coordinates of found</p>
<p>WAP’s if the a GPS receiver is connected to your device.</p>
<h3 id="ulogging-and-event-viewing-toolsu"><u>Logging and Event Viewing Tools</u></h3>
<p><strong>Log Parser Lizard</strong>: A Microsoft based log viewing tool that presents the information in a GUI</p>
<p>based format. It’s capable of presenting data from individual systems, SQL servers, AD, IIS,</p>
<p>and many other types of log / event creating applications or systems.</p>
<p><strong>Splunk</strong>: An enterprise tool used to store and parse logs on a large scale to monitor network</p>
<p>activity and functionality.</p>
<p><strong>SolarWinds</strong>: An enterprise tool similar to Splunk, with the exception that it can create a</p>
<p>database for network monitoring. It’s useful in visualizing the configuration of the network in</p>
<p>a live environment which reduces the need for static network topology tools like Vizio.</p>
<h3 id="uother-toolsu"><u>Other Tools</u></h3>
<p><strong>Snort</strong>: A freeware IDS / IPS.</p>
<p><strong>Metasploit</strong>: This is an automated framework capable of exploiting vulnerabilities with many</p>
<p>tools across many platforms.</p>
<h3 id="uhardware-toolsu"><u>Hardware Tools</u></h3>
<p><strong>Minipwner</strong>: A small device that can be connected to the target network and left behind to</p>
<p>allow the actor to gather information remotely. It can be configured with battery or power</p>
<p>cord. It’s low power consumption allows the device to be used a WAP on battery power for</p>
<p>several hours.</p>
<p><strong>USB Rubber Ducky</strong>: A flash drive that is recognized as a Human Interface Device (HID). It</p>
<p>can bypass most enterprise DLP software since the software thinks the device is a keyboard.</p>
<p>It is capable of running scripts and gathering data among many other uses that can be</p>
<p>dreamt up for it.</p>
<p><strong>Wi-Fi Pineapple</strong>: A small discrete device that has powerful application for pentesting. It can</p>
<p>be used as a potential Evil Twin WAP. It comes with an impressive suite of applications that</p>
<p>helps to analyze the data collected by the device.</p>
<p><strong>LAN Turtle</strong>: A Small USB-to-Ethernet adapter that can be placed on a victims computer</p>
<p>inside the target network. I can fingerprint and enumerate the network and be used to create</p>
<p>an SSH into the network. It can also spoof DNS entries on the network for a redirection /</p>
<p>session hijacking attack.</p>
<p><strong>AirPcap</strong>: A USB designed to provide a hardware based pentesting tool. It works in</p>
<p>conjunction with other common tools. It can be used on wireless networks and may conduct</p>
<p>packet injection to active connections. It can function as an Evil Twin, or Rogue AP.</p>
<p><strong>Ubertooth One</strong>: A USB device that can be used to scan for Bluetooth communication.</p>
<h3 id="table-of-contents"><a href="https://karsyboy.github.io/CEHv10_Ultimate_Study_Guide/">Table Of Contents</a></h3>

