## Exam 

1. Why do we need layered protocols organization for communications, e.g., OSI?
> The data is passed from the upper layer to lower layer through an interface. A Layered architecture provides a clean-cut interface so that minimum information is shared among different layers. It also ensures that the implementation of one layer can be easily replaced by another implementation [source](https://www.javatpoint.com/computer-network-models#:~:text=A%20Layered%20architecture%20provides%20a,is%20known%20as%20network%20architecture)
> 
Why do we require Layered architecture?
 - Divide-and-conquer approach: Divide-and-conquer approach makes a design process in such a way that the unmanageable tasks are divided into small and manageable tasks. In short, we can say that this approach reduces the complexity of the design.
 - Modularity: Layered architecture is more modular. Modularity provides the independence of layers, which is easier to understand and implement.
 - Easy to modify: It ensures the independence of layers so that implementation in one layer can be changed without affecting other layers.
 - Easy to test: Each layer of the layered architecture can be analyzed and tested individually.

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
>

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
> 
> https://www.serverbrain.org/network-design-2003/to-network-id-or-host-id-that-is-the-question.html

8. Why are two subnetwork addresses reserved in any subnetwork? Which are those?
> 

9. Which of these subnets have more addressed for hosts: 10.0.0.0/8 or 172.16.0.0/12?
>

10. What is the difference between congestion control and flow control?
>

11. What is the basic principle of window-based flow control?
>

12. Which explicit congestion control mechanisms available for TCP?
>

13. Why do we need the slow start phase in TCP?
>

14. What are the two service models in the Internet?
>

15. Choose ands briefly describe one application layer protocol.
> 
