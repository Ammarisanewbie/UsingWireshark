# Using Wireshark for Capturing and Examining Packets

## Introduction
The purpose of this project is to utilise and familiarise with Wireshark and it's basic functions.
Wireshark is one of the most common packet sniffer and analysis tools used by most Cybersecurity professionals (Red & Blue team).
It records connections such as Bluetooth, Ethernet, and wireless to name a few, and saves the information for further analysis (usually in a .pcap file)

 ## Software and Tools Used
 - Wireshark

## Objectives
1. Basic Packet Capturing
2. Using Display Filters
3. Using Conditional Statements and Operators

## Software Walk-through
- Remember to update after installation to ensure you have the most stable and updated version
- After installation, add a user to the wireshark group to enable Least Privileges control.
- *_Important: Do not run wireshark as a superuser for security reasons_ 

## 1. Basic Packet Capturing
-	The wired interface includes the ethernet packet capture, which begins with ‘en’ in Wireshark.
-	The Wireshark app includes controls to start packet capture, stop capture, save the packets to a file, and load the capture file.
-	A capture can only be saved once the capture has stopped.

 ![2023-12-20_15-01](https://github.com/anmelson/UsingWireshark/assets/108499824/3b6a0e06-12cd-4304-9bdc-cd8bb79768a0)


## 2. Using Display Filters

### Using display filter
- To display only HTTPS traffic, use a filter on TCP port 443: tcp.port == 443.

 ![Picture1](https://github.com/anmelson/UsingWireshark/assets/108499824/80d9fd0d-4610-48cf-9593-4a888114f497)

- To display traffic associated with a specified IP address, display filter: **ip.addr ==** _enter ip_.
- To display only the destination address, display filter: **ip.dst==** _enter dst ip_.

### Basic Analysis - Examining the Client Hello packet (TLS handshake)
- A TLS handshake display filter may be used to detect a website visit in a packet list:
** tls.handshake.type ==1** > to check for ‘Client Hello’ aka HTTPS handshake protocol
  
 ![ClientHello](https://github.com/anmelson/UsingWireshark/assets/108499824/4fbe02f5-0fd2-4e3f-bcf3-31804081bfdb)

- Further details such as Src and Dst IP, Src,Dst Port and Packet length can be found
  
 ![Picture3](https://github.com/anmelson/UsingWireshark/assets/108499824/eec56313-c010-4cd4-afd8-cce16c0b02d9)

## 3. Using Conditional Statements and Operators
- Filtering out a specific IP address or any HTTPS traffic.

 ![2023-12-20_14-59](https://github.com/anmelson/UsingWireshark/assets/108499824/af325e72-97b7-42c9-a743-20aed76a7e9f)

- Filtering out an IP address while displaying HTTPS and HTTP traffic

 ![Picture4](https://github.com/anmelson/UsingWireshark/assets/108499824/6a8b6763-93b7-4a90-b6f1-63807d508942)
 
## Conclusion
To more effectively analyse network traffic from saved capture files or live capture data, this project has helped me become familiar with the different filters that Wireshark can do. Being proficient with Wireshark is a crucial ability for any cybersecurity specialist.
  

