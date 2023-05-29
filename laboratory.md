**Question 1**  

Choose the best matching explanation for each term related to IP networks.

Multicast:  one sender, multiple receivers in a specified group of receivers
 
Broadcast : one sender, multiple receivers
 
Anycast : one sender, one receiver in a specified group of receivers
 
Unicast : one sender, one receiver


**Question 2**

Choose the best matching explanation for each term related to IP subnetworks.

Broadcast address : last address of the subnetwork
 
Last host address: second to last address of the subnetwork
 
First host address: second address of the subnetwork
 
Network address : first address of the subnetwork
 
 
**Question 3**

Find out the network mask, network address and broadcast address related to the following IP address. Give all answers in decimal format a.b.c.d.
```
10.1.4.123/24
network mask	: 255.255.255.0

network address	: 10.1.4.0

broadcast	: 10.1.4.255
```
 
**Question 4**

Choose the best matching explanation for each term related to IP networks.

```
DHCP : used to assign an IP address to a device
 
ARP : used to map MAC addresses to IP addresses
 
IP address : network layer address
 
MAC address : link layer address
``` 
  
**Question 5**  

Choose the best matching explanation for each networking device.
```
Router : forwards packets based on their destination IP address
 
Hub : broadcasts every packet received
 
Switch : forwards packets based on their destination MAC address
```

**Question 6**

What does the switch do if it doesn't know which port it should use to reach the destination device?

```
a.It sends an error message to the sender of the packet as an ICMP packet. -- wrong

b.It sends an ARP packet as broadcast requesting the MAC address of the destination device.

c.It sends a packet from all ports in the same way as a broadcast. -- next?

d.It queries the device that sent the packet for the correct destination using an ARP packet.

e.It discards the packet. -- wrong  
```

**Question 7**

Which of the following IP addresses belong to the same network as the server 192.168.1.10/25?
```
Select one or more:

a.192.168.1.255

b.192.168.1.200

c.192.168.0.10

d.10.0.1.10

e.192.168.1.0 --

f.192.168.1.123 --

g.192.168.1.1 --

h.192.168.2.10
```

**Question 8**

The network 10.0.0.0/24 will be split into to two equally sized subnetworks. What are the resulting subnetworks?
```
Select one:

a.The network cannot actually be split into two equally sized subnetworks.

b.10.0.1.0/24 and 10.0.2.0/24

c.10.0.0.0/12 and 10.0.0.0/12

d.10.0.0.0/24 and 10.0.0.128/24

e.10.0.0.0/25 and 10.0.0.128/25 --

f.10.0.0.0/25 and 10.0.1.0/25
```

**Question 9**  

Observe the network shown in the picture above. Workstation A sends an ICMP packet to workstation B. What are the IP and MAC addresses written in the packet as the packet passes through link L2?

![image](https://github.com/saugkim/2023summer_COM_NET_tuni/assets/25344978/29b9b06c-d1a6-4474-862c-57c13e32a15c)
```
Source IP == 10.0.0.123
 
Destination IP == 192.168.0.123
 
Source MAC ==  11:11:11:00:00:bb
 
Destination MAC ==  22:22:22:00:00:bb
```


**Question 10**

Imagine that your PCs IP address is 130.230.83.12/25 and you have just joined the network (= all caches are empty). Your default gateway is set to 130.230.83.1. You want to send packets to the hosts listed below. You will be sending the packets in the order listed a few seconds after each other. Choose the first action that happens with each packet from the list of actions given.

``` 
130.230.83.2 != forward packet to default gateway
             != query default gateway with ARP
             == query host with ARP 
  
8.8.8.8 != query host with ARP 
        != forward packet to default gateway
        != drop the packet
 
130.230.83.200 != query default gateway with ARP 
               != query host with ARP
               != change destination IP to default gateway
 
130.230.83.2 (again) = send packet directly to host
```

**Question 11**

Your router has the following simplified routing table:

|Destination	|Next hop|
|:-- | -:|
|0.0.0.0/0	|1|
|192.168.0.0/16  	|2|
|172.16.0.0/12|	3|
|8.8.8.8/32	|4|
|10.0.0.0/8	|5|
|10.0.0.0/16	|6|
|10.0.0.0/24	|7|


Mark the next hop for packets sent to the following addresses. Mark 0, if the packet is dropped because it does not match any rule. In the case two or more rules match, the most specific one takes priority (= longest network mask).

```
Destination IP  	Next hop

192.168.1.1	Answer == 2

10.1.1.10	  Answer == 5

10.0.10.0	  Answer == 6

1.2.3.4	    Answer == 1 

10.0.1.1	   Answer == 6

8.8.8.8	    Answer == 4

172.32.0.1	Answer == 1
```

 
**Question 12**

You are connecting two devices together with an Ethernet cable. Mark the situations where you should use a crossover cable instead of a "normal" straight-through cable. Assume that Auto MDI-X is not enabled.

(This question has been included for historical purposes, as it is not relevant for the remote lab. Moreover, thanks to the Auto MDI-X feature, this is not very important anymore in practical networks either, but it's "good to know just in case".)

```
Select one or more:

a.switch to router -- wrong

b.router to router  --yes
 
c.router to PC  -- yes

d.PC to PC -- yes

e.switch to switch -- yes

f.switch to PC -- wrong
```
