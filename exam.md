## Exam 

1. Why do we need layered protocols organization for communications, e.g., OSI?
> The data is passed from the upper layer to lower layer through an interface. A Layered architecture provides a clean-cut interface so that minimum information is shared among different layers. It also ensures that the implementation of one layer can be easily replaced by another implementation [source](https://www.javatpoint.com/computer-network-models#:~:text=A%20Layered%20architecture%20provides%20a,is%20known%20as%20network%20architecture)
> 
> Why do we require Layered architecture?
> - Divide-and-conquer approach: Divide-and-conquer approach makes a design process in such a way that the unmanageable tasks are divided into small and manageable tasks. In short, we can say that this approach reduces the complexity of the design.
> - Modularity: Layered architecture is more modular. Modularity provides the independence of layers, which is easier to understand and implement.
> - Easy to modify: It ensures the independence of layers so that implementation in one layer can be changed without affecting other layers.
> - Easy to test: Each layer of the layered architecture can be analyzed and tested individually.

2. Name at least two link-layer network topologies. Discuss advantages and shortcomings.
> **Types of Network Topology**  
> The arrangement of a network that comprises nodes and connecting lines via sender and receiver is referred to as Network Topology. The various network topologies are:
> - Point to Point Topology
> - Mesh Topology
> - Star Topology
> - Bus Topology
> - Ring Topology
> - Tree Topology
> - Hybrid Topology
>  
> link-layer network topologies [source](https://www.geeksforgeeks.org/types-of-network-topology/) 

3. Why does IEEE standardize only two lower layers in Wi-Fi?
> IEEE 802 specifications are focused on the two lowest layers of the OSI model because they incorporate both physical and data link components.
> https://www.linkedin.com/pulse/internet-things-part-12-mahendra-bhatia#:~:text=IEEE%20802%20specifications%20are%20focused,physical%20and%20data%20link%20components.  
> https://www.scaler.com/topics/computer-network/ieee-standards-in-computer-networks/

4. What are the functionalities of network (IP) layer?
> The main function of the network layer or layer 3 of the OSI (Open Systems Interconnection) model is delivery of data packets from the source to the destination across multiple hops or links. It also controls the operation of the subnet.
>
> The functions are elaborated as below   
> - When data is to be sent, the network layer accepts data from the transport layer above, divides and encapsulates it into packets and sends it to the data link layer. The reverse procedure is done during receiving data.
> - The network layer is responsible for routing packets from the source host to the destination host. The routes can be based upon static tables that are rarely changed; or they can be automatically updated depending upon network conditions.
> - Many networks are partitioned into sub-networks or subnets. The network layer controls the operations of the subnets. Network devices called routers operate in this layer to forward packets between the subnets or the different networks.
> - The lower layers assign the physical address locally. When the data packets are routed to remote locations, a logical addressing scheme is required to differentiate the source system and the destination system. This is provided by the network layer.
> - This layer also provides mechanisms for congestion control, in situations when too many packets overload the subnets.
> - The network layer tackles issues like transmission delays, transmission time, avoidance of jitters etc.
>
> https://www.tutorialspoint.com/functions-of-the-network-layer 

5. Can two consecutive IP packets from a single source take different path in network?
Why or why not?
> Can two packets from the same device take different routes?  
> - Each router examines and sends each IP packet individually — this is called packet switching. If the network changes, due to congestion or faults, routers can use an alternative interfaces to reach a destination. So packets may travel over different routes to reach the same destination.   
> https://www.futurelearn.com/info/courses/introduction-to-networking/0/steps/53448
>
> Can packets be sent along different paths?
> - Different paths can be used to route packets to their destination. This process is known as packet switching. If an error occurs, the packets can be stored and retransmitted later. Packets use the best route available for delivery.
> https://www.techtarget.com
>
> Why do data packets travel along different paths to get to your computer?
> - Packet switching is the transfer of small pieces of data across various networks. These data chunks or “packets” allow for faster, more efficient data transfer. Often, when a user sends a file across a network, it gets transferred in smaller data packets, not in one piece.  
> https://avinetworks.com/glossary/packet-switching/
> 
> Do packets always take the same route from sender to receiver?  
> - Information on the Internet is not sent all at once, but is instead broken into smaller chunks of data called packets. Each packet is sent through the Internet individually and may actually take different paths or arrive at different times than others. Once they arrive the receiver will use the packets to recreate the original file.  
> https://quorumlanguage.com/lessons/code/Digital-Information/Lesson5.html

6. Which protocol is utilized in tracert (traceroute) routines? How does they work?
>  https://www.fortinet.com/resources/cyberglossary/traceroutes  
>  A traceroute works by sending Internet Control Message Protocol (ICMP) packets, and every router involved in transferring the data gets these packets. The ICMP packets provide information about whether the routers used in the transmission are able to effectively transfer the data.
>
> A traceroute provides a map of how data on the internet travels from its source to its destination.  When you connect with a website, the data you get must travel across multiple devices and networks along the way, particularly routers.
>
> A traceroute plays a different role than other diagnostic tools, such as packet capture, which analyzes data. Traceroute differs in that it examines how the data moves through the internet. Similarly, you can use Domain Name System time to live (DNS TTL) for tracerouting, but DNS TTL addresses the time needed to cache a query and does not follow the data path between routers.
>
> https://www.fortinet.com/resources/cyberglossary/traceroutes


7. Why two logical parts an IP address consists of? Why do we need that?
> The bytes of the IP address are further classified into two parts: the network part and the host part. Figure 3-1 shows the component parts of a typical IP address, 129.144.50.56.
> https://docs.oracle.com/cd/E19504-01/802-5753/planning3-18471/index.html
>  
> Network Part  
> - This part specifies the unique number assigned to your network. It also identifies the class of network assigned. In Figure 3-1, the network part takes up two bytes of the IP address.
>
> Host Part
> - This is the part of the IP address that you assign to each host. It uniquely identifies this machine on your network. Note that for each host on your network, the network part of the address will be the same, but the host part must be different.
>  
> Why do we need network ID?
> - An IP address consists of two components: a network ID and a host ID. The network ID identifies the network segment to which the host belongs. The host ID identifies an individual host on some specific network segment. A host can communicate directly only with other hosts on the same network segment. A network segment is a logical division of a network into unique numeric network IDs called subnets. A host must use a router to communicate with hosts on other subnets.  
> https://www.serverbrain.org/network-design-2003/to-network-id-or-host-id-that-is-the-question.html

8. Why are two subnetwork addresses reserved in any subnetwork? Which are those?
> For largely historical reasons, two addresses are reserved on every subnet.   
> They are the smallest and largest addresses - those two with all 0s and all 1s in the host field (the bits to the right of the prefix boundary). No host can be assigned either of these reserved addresses.  
> The all 0s address was used by older routing protocols to distinguish a subnet route from a 32-bit host route. The all 1s address was used to broadcast to all hosts on the subnet.  
> https://www.freesoft.org/CIE/Course/Subnet/103.htm


9. Which of these subnets have more addressed for hosts: 10.0.0.0/8 or 172.16.0.0/12?
> 10.0.0.0/8
```
Address:   10.0.0.0              00001010 .00000000.00000000.00000000
Netmask:   255.0.0.0 = 8         11111111 .00000000.00000000.00000000
Wildcard:  0.255.255.255         00000000 .11111111.11111111.11111111
=>
Network:   10.0.0.0/8            00001010 .00000000.00000000.00000000 (Class A)
Broadcast: 10.255.255.255        00001010 .11111111.11111111.11111111
HostMin:   10.0.0.1              00001010 .00000000.00000000.00000001
HostMax:   10.255.255.254        00001010 .11111111.11111111.11111110
Hosts/Net: 16777214              (Private Internet)
```
> 172.16.0.0/12
```
Address:   172.16.0.0            10101100.0001 0000.00000000.00000000
Netmask:   255.240.0.0 = 12      11111111.1111 0000.00000000.00000000
Wildcard:  0.15.255.255          00000000.0000 1111.11111111.11111111
=>
Network:   172.16.0.0/12         10101100.0001 0000.00000000.00000000 (Class B)
Broadcast: 172.31.255.255        10101100.0001 1111.11111111.11111111
HostMin:   172.16.0.1            10101100.0001 0000.00000000.00000001
HostMax:   172.31.255.254        10101100.0001 1111.11111111.11111110
Hosts/Net: 1048574               (Private Internet)
```
> Netmask 8 has a lot more number of hosts available than Netmask 12  
> https://jodies.de/ipcalc



10. What is the difference between congestion control and flow control?
>

11. What is the basic principle of window-based flow control?
>

12. Which explicit congestion control mechanisms available for TCP?
>

13. Why do we need the slow start phase in TCP?
>

14. What are the two service models in the Internet?
> traditional lightweight service model
> heavyweight grid service model 
> https://www.cs.cmu.edu/afs/cs/project/cmcl/archive/Remulac-papers/msu99/sld015.htm
>
> 

15. Choose ands briefly describe one application layer protocol.
> 
