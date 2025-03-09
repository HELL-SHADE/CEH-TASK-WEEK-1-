# CEH-TASK-WEEK-1-
# Welcome to the CEH-TASK-WEEK-1- wiki!
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

## Summary
TCP and UDP serve different purposes in network communication. TCP is ideal for those applications where reliability and data integrity are important, while UDP is better suited for those applications where speed and efficiency are more critical than reliability. 

#  List the TCP Flags along with their use/function?
