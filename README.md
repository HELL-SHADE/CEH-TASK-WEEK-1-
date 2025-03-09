#  CEH-TASK-WEEK-1-
##  Discuss TCP & UDP Protocols and mention the difference between the two along with examples where they are used?
### **TCP (Transmission Control Protocol)**
1.  TCP make a connection between the sender and receiver before data transfer begins by a three-way handshake: SYN, SYN-ACK, ACK.
2.  TCP make ensures that data is delivered accurately and in order.
3.  TCP has higher overhead making it slower compared to UDP.

## TCP (Transmission Control Protocol) EXAMPLES :-
1. Web browsing (HTTP/HTTPS)

2. Email (SMTP, IMAP, POP3)

3. File transfer (FTP)

4. Remote access (SSH, Telnet)

## UDP (User Datagram Protocol)
1.  UDP does not establish a connection before sending data. It simply sends packets to the receiver.

2.  UDP does not guarantee delivery of packets and not checking errors, Packets can be lost.

3.  UDP has minimal overhead, making it faster and more efficient for some applications.


## UDP (User Datagram Protocol) EXAMPLES :- 
1.  Video streaming (e.g., YouTube, Netflix)

2.  Online gaming

3.  Voice over IP (VoIP) (e.g., Skype, Zoom)

4.  DNS queries

5.  Real-time communication (e.g., live broadcasts)



# When to Use TCP vs. UDP
## Use TCP when:

1.  Data integrity and reliability are critical (e.g., file transfers, web browsing).

2.  The order of data delivery matters (e.g., database transactions).

3.  The application can tolerate some delay (e.g., email).

## Use UDP when:

1.  Speed and low latency are more important than reliability (e.g., video streaming, online gaming).

2.  Real-time communication is required (e.g., VoIP, live broadcasts).

3.  The application can handle packet loss or out-of-order delivery (e.g., DNS queries).



#  List the TCP Flags along with their use/function?

### TCP (Transmission Control Protocol) uses several flags to control the state of a connection and manage data flow. Each flag is a single bit in the TCP header, and they serve specific purposes during communication. 

### Here are the TCP flags along with their functions:

### 1.  URG (Urgent):

Indicates that the urgent pointer field is significant.
Used to prioritize certain data. When set, the receiving system should process the urgent data immediately.

### 2.  ACK (Acknowledgment):

Acknowledges the receipt of data.
Indicates that the acknowledgment number in the TCP header is valid. This flag is set in most packets after the initial SYN packet in a connection.

### 3.  PSH (Push):

Requests the receiving system to push the data to the application immediately.
Ensures that data is delivered to the application without waiting for the buffer to fill. This is useful for real-time applications.

### 4.  RST (Reset):

Resets the connection.
Used to abruptly terminate a connection, usually in response to an error or an unexpected condition.

### 5.  SYN (Synchronize):

Initiates a connection between hosts.
Used during the three-way handshake to synchronize sequence numbers and establish a connection.

### 6.  FIN (Finish):

Signals the end of a connection.
Used to gracefully close a connection. When a host sends a FIN flag, it indicates that it has no more data to send.

## What is the difference in executing nmap as root user and as normal user? Give the flags in nmap which require root permission to be performed?
### Executing nmap as a root user versus a normal user can result in significant differences in functionality, particularly because certain advanced scanning techniques and options require elevated privileges.

### Nmap Flags That Require Root Permissions:
1.  SYN Scan (-sS):
A stealthy scan that sends SYN packets without completing the TCP handshake. Requires root to send raw packets.

2.  UDP Scan (-sU):
Scans UDP ports, which requires raw packet sending.

3.  IP Protocol Scan (-sO):
Determines which IP protocols (e.g., TCP, UDP, ICMP) are supported by the target.

4.  Idle Scan (-sI):
Uses a zombie host to scan the target stealthily.

5. OS Detection (-O):
Detects the operating system of the target by analyzing TCP/IP stack behavior.

6. ARP Scan (-PR):
Sends ARP requests to discover hosts on the local network.

7.  Packet Tracing (--packet-trace):
Traces the packets sent and received during the scan.

8.  Custom TCP Flags (--scanflags):
Allows setting custom TCP flags in packets.

9.  Fragment Packets (-f):
Fragments packets to evade detection.

10.  Decoy Scans (-D):
Hides the scan among decoy IP addresses.

11.  Spoofing Source IP (-S):
Spoofs the source IP address of the scan.

12.  Timing and Performance Options (-T):
Aggressive timing options (-T4, -T5) may require root for faster scans.

## Example Commands Requiring Root:
1.  SYN Scan: sudo nmap -sS <target>

2.  UDP Scan: sudo nmap -sU <target>

3.  OS Detection: sudo nmap -O <target>

4.  Idle Scan: sudo nmap -sI <zombie> <target>

## Summary:
Root privileges are required for advanced scanning techniques, raw packet manipulation, and low-level network operations.

Normal users are limited to basic scans like TCP connect scans (-sT) and lack the ability to perform stealthy or advanced scans.
