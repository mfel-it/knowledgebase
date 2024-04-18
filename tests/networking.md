# Networking

**Fundamentals**

* What is the difference between TCP and UDP? When would you use one over the other? (Reliable vs. unreliable transmission)
* Describe the purpose of subnetting and how it affects IP addressing. (Network segmentation)
* How do routers and switches work together to facilitate network traffic? (Layer 2 vs. Layer 3 devices)
* What is DNS, and how does it function? (Translating domain names to IP addresses)

**Network Design & Protocols**

* Discuss factors to consider when choosing between wired and wireless networks. (Speed, security, mobility, cost)
* Explain the concepts of NAT (Network Address Translation) and PAT (Port Address Translation). (Conserving public IP addresses)
* What is DHCP, and how does it automate IP address configuration? (Dynamic host configuration)
* Describe common routing protocols like OSPF and BGP. (Path determination within networks and between networks)
* What is network topology, and how do different topologies (e.g., star, bus, mesh) affect performance and redundancy?

**Security**

* How do firewalls protect a network? What are different types of firewalls? (Packet filtering, stateful inspection)
* What is a VPN, and how does it provide secure remote access? (Encryption and tunneling)
* Discuss common network security threats like malware, DDoS attacks, and intrusions.
* What is network segmentation, and how does it enhance security? (Isolating sensitive assets)
* Explain the concept of network access control (NAC) (Controlling device access to the network)

**Troubleshooting**

* You have intermittent network connectivity issues. What are the first steps you would take to troubleshoot? (Physical checks, ping, traceroute)
* What tools would you use to diagnose slow network performance? (Packet analyzers, bandwidth monitoring)
* A user reports they cannot access a specific website. Describe your troubleshooting process. (DNS resolution, firewalls, application issues)
* How can you identify potential security breaches on your network? (Intrusion detection systems, log analysis)

**VLANs**

* What is a VLAN, and what are the benefits of using them? (Segmentation, security, flexibility)
* How do you configure a VLAN on a switch? What is the role of trunking? (Port assignments, tagging for cross-switch traffic)
* Describe a scenario where using multiple VLANs could improve network performance and security.
* What is inter-VLAN routing, and how is it achieved? (Layer 3 devices facilitating communication between VLANs) 

**OSI Model**

* Explain the OSI model and the function of each layer. (Understanding the theoretical framework)
* A malfunctioning network cable would affect which layer of the OSI model? (Physical Layer)
* Modifying a firewall rule operates at which layer of the OSI model? (Transport or Network depending on rule type)
* Describe a networking problem that could be caused by an issue at the Application layer of the OSI model. (Web server misconfiguration, corrupt file transfer)
* How does the OSI model help troubleshoot a network problem in a structured manner? (Isolation of the issue to a specific layer)

**SNAT vs. DNAT**

* Explain the primary use case for SNAT (Source Network Address Translation). (Many internal devices sharing a single public IP)
* Describe the primary use case for DNAT (Destination Network Address Translation). (Making internal servers accessible from the internet)
* Provide a scenario where you might use both SNAT and DNAT in conjunction. (Internal server accessible from outside, but conserving public IPs)
* What configuration changes are typically made on a firewall or router to implement SNAT and DNAT? (Address/port mapping rules)

**Networking Tools**

* Name three common command-line tools for diagnosing network issues and provide their typical use cases. (ping, ipconfig/ifconfig, traceroute/tracert)
* What is a packet analyzer (e.g., Wireshark), and how is it used for troubleshooting? (Deep inspection of network traffic)
* Describe network monitoring tools and what key metrics they track. (Bandwidth usage, device uptime, packet loss, alerts) 
* What tools might you use to troubleshoot wireless network performance? (WiFi analyzers, site survey tools)

## Wi-Fi Networking

**Fundamentals**

* What is the difference between the 2.4 GHz and 5 GHz Wi-Fi bands? (Coverage vs. speed, interference susceptibility)
* Explain the concept of Wi-Fi channels and why it's important to choose the right ones. (Minimizing interference)
* What factors can affect Wi-Fi signal strength and range? (Obstacles, distance, antenna type)
* Describe the different Wi-Fi security standards (WEP, WPA, WPA2, WPA3). (Evolution of encryption and protection)

**Configuration & Troubleshooting**

* You're experiencing slow Wi-Fi speeds. What are the first few things you would check? (Device distance, channel congestion, router settings)
* What steps would you take to secure your home Wi-Fi network? (Strong password, WPA2 or higher, updating router firmware)
* How do you identify which devices are connected to your Wi-Fi network? (Accessing router's interface)
* Describe a scenario where using a Wi-Fi extender or mesh network might be beneficial. (Large homes, dead zones)

**Advanced Topics**

* What is the difference between a Wi-Fi router and a Wi-Fi access point? (Routing functionality vs. wireless signal broadcasting)
* Explain the concepts of MU-MIMO and beamforming. (Modern Wi-Fi technologies for improved multi-device performance)
* Discuss the advantages and disadvantages of the new Wi-Fi 6 (802.11ax) standard. (Higher speeds, better device capacity, but compatibility)
* How can you troubleshoot Wi-Fi interference from non-Wi-Fi sources (e.g., microwaves)? (Spectrum analyzers, changing channels)

**Practical Scenarios**

* You're setting up Wi-Fi in a multi-story house. What factors do you consider for optimal router placement?
* You're working in a crowded office environment with many Wi-Fi networks. How can you optimize your network's performance?
* You need to provide guest Wi-Fi access but want to keep it securely separated from your main network. How would you achieve this? 
