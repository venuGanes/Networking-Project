# Cisco Router & Switch Configuration with Internet Access — Router-on-a-Stick Method

# Objective
To provide a comprehensive, beginner-friendly walkthrough for configuring Cisco routers and switches using the Router-on-a-Stick method, enabling VLAN segmentation, DHCP services, and Internet connectivity for small to medium-sized networks.

# Purpose
I created this to share what I’ve learned about setting up Cisco networking devices in a real-world scenario. This includes configuring VLANs, trunk/access ports, DHCP services, IP addresses, and connecting everything to the internet.

![Alt text](https://github.com/venuGanes/Networking-Project/blob/3b491b029588706dc9ac80887c4457f227f40637/IMG%201.png)

1) connect router FA0/0 port to port 10 of switch 1 (ISP Router) connected to LAN 

2) Connect fa0/1 of router to port 48 of Switch 2 (trunk) 

3) fa 0/0 has been configured 103.249.93.68 255.255.255.248, gateway 103.249.93.65 

4) Next, connect from router to laptop via console port 

5) Identify the port number and connect via PuTTY

![Alt text](https://github.com/venuGanes/Networking-Project/blob/6be1f04809415c266433c282a4de8b35dcbcad64/IMG%202.png)

6) sh ip int br  to view the configurations

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%203.png)

7) to allow any ip to go through the gateway 103.249.93.65

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%204.png)

8) configuring sub int vlan 10 – 30

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%205.png)

9)create pool for each vlan 

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%206.png)

Vlan 10 gateway add 
![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%207.png)

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%208.png)

10) configure nat 

#Int fa0/0 on router 

#Ip nat outside 

#Int fa0/1.10 - 30 

# ip nat inside 

11) configure acl

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%209.png)

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2010.png)

12) next, switch console cable to switch2 

Configure it as trunk 
 
![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2011.png)

13)
 
![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2012.png)  

14) create vlan with no shut command

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2013.png)  

15) configure int of vlan

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2014.png)  

16) test connectivity 

Vlan 10 

![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2015.png) 

Vlan 20 
![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2016.png) 

Vlan 30 
![Alt text](https://github.com/venuGanes/Networking-Project/blob/9a526f10713bc6948757d19d101bf3a3db9007cc/IMG%2017.png) 

