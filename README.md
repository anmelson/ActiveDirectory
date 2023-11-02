# Active Directory

A project designed to expand working knowledge of Active Directory.

## Description

The goal of this project is an in depth look into the fucntions and features of Active Directory, along with a lab implementation component.   

## Languages and Utilities Used

- **Microsoft Active Directory**

## Program Walk-through

### To begin, we take the role of soemone at the Help Desk who has just recieved the following email

![Received Email](https://i.imgur.com/Cw4b8F4.png)

### 

![Searching for Conversations by limiting displayed data](https://i.imgur.com/wDRoD67.png)

### From there, we can see the following requests come through, with the first completed three way handshake happening on HTTP to 95.216.26.30

![Completed Three Way Handshake](https://i.imgur.com/CooHQN5l.png)

### Next, we determined the timestamp of the first conversation. I used the -tttt switch to make the data more readable:

![Timestamp](https://i.imgur.com/T6hyc4p.png)

### The next goal was to find the DNS request for apache.org and determine the IP address/s of the website.  I filtered the traffic for port 53 (DNS) to make the search easier and found the resulting A record request

![IP address](https://i.imgur.com/mcjKudT.png)

### Lastly, I was asked to examine the ASCII code of the packets using the -X switch to find any information about the webserver, such as the name which can be seen here

![Webserver Info](https://i.imgur.com/DXTSGYql.png)

### Moving on to Wireshark, we applied a simple HTTP filter to a pcap file

![tcp.port == 80 filter](https://i.imgur.com/Cz9zfMbl.png)

### I was then tasked with following the TCP stream of one of the OK responses and look for JFIF files.

![Searching for JFIFs in the TCP Stream](https://i.imgur.com/TcR0dwhl.png)

### Knowing files were transferred, we saved copies of these JPG files.

![Saving the JPGs](https://i.imgur.com/coXefesl.png)

### Next, we RDPed into another system to run Wireshark on that system to search for malicious activity

![RDPing in to run a capture](https://i.imgur.com/hV25xfzl.png)

### The goal was to search the traffic to find the employee responsible, so I followed the tcp stream

![TCP Steam Followed](https://i.imgur.com/WxNV1S3l.png)

### As we can see, a user has been created and added to the administrator account through a host machine

![User created and given privileges](https://i.imgur.com/ZO2wbDml.png)

### Our last goal was to decrypt RDP traffic using a provided key and pcap file, so first we checked to see if there was RDP traffic using port 3389, since the rdp protocol is encrypted

![Isolating RDP traffic](https://i.imgur.com/GD1VCx3l.png)

### Adding the RSA TLS key to Wireshark

![Adding the RSA Key](https://i.imgur.com/YZNxCyDl.png)

### Now that we have applied the key, rdp traffic is visible

![RDP traffic shows up](https://i.imgur.com/Q9T6uAsl.png)

### After determing the host that initiated the connection, we reexamined traffic through the filter tcp.port == 3389 to try and find a username. Examing the Ignored Unknown Request packet, we can see it in ASCII

![Host Username](https://i.imgur.com/zq7290Il.png)

## Conclusion
