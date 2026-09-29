network-attack-incident-report.md.
Cybersecurity Incident Report 
 
Section 1: Identify the type of attack that may have caused this  
network interruption 
One potential explanation for the website's connection timeout error message is 
 
The logs show that: Starting at packet 52 (about 3.39s), IP 203.0.113.0 sends a continuous 
stream of TCP SYN packets to the web server at 192.0.2.1, all from port 54770 to 443. The 
same address sent about 140 SYN packets and never completed a handshake. Normal 
visitors (198.51.100.x) completed handshakes and got 200 OK early on. After the flood 
began, their connections failed with RST, ACK resets, and a 504 Gateway Time-out.  
 
This event could be :   A TCP SYN flood attack, which is a type of denial of service (DoS) 
attack. The traffic comes from a single IP address (203.0.113.0), so it is DoS rather than 
DDoS.  
 
 
Section 2: Explain how the attack is causing the website to malfunction 
When website visitors try to establish a connection with the web server, a three-way 
handshake occurs using the TCP protocol. Explain the three steps of the handshake: 
1. The client sends a SYN packet to the server to request a connection.  
 
2. The server replies with a SYN-ACK packet to acknowledge the request and reserve 
resources for the connection.  
 
3. The client sends a final ACK packet to confirm, and the connection is established.  
 
Explain what happens when a malicious actor sends a large number of SYN packets all at 
once: The server replies to each SYN with a SYN-ACK and waits for the final ACK, which 
never arrives. These half-open connections fill the connection queue and use up the 
server's resources, so it can't accept new connections  
 
Explain what the logs indicate and how that affects the server: The logs show 203.0.113.0 
sending a continuous flood of SYN packets with no completing ACKs. Legitimate visitors 
start receiving RST, ACK resets, and a 504 Gateway Time-out. The server is overwhelmed, 
and the website becomes unavailable, causing connection timeout errors.  
 
