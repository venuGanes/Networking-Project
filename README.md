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

