## Protocol Layers

Distributed systems are hard. There are multiple computers involved, which have to be connected in some way. Programs have to be written to run on each computer in the system and they all have to co-operate to get a distributed task done.

分布布系统是有难度的。包含了多台计算机，每台计算机以某种方式相连。编写的程序必须在系统中的每台计算机上运行，程序间通过合作完成分布式任务。

The common way to deal with complexity is to break it down into smaller and simpler parts. These parts have their own structure, but they also have defined means of communicating with other related parts. In distributed systems, the parts are called protocol layers and they have clearly defined functions. They form a stack, with each layer communicating with the layer above and the layer below. The communication between layers is defined by protocols.

处理复杂性更普遍的方法是将其分解为小和简单的模块。这些模块有他们自己的结构，但他们也定义了和其它相关模块通信的方法。在分布式系统中，这些模块被称为协议层，它们清晰地定义了功能。他们形成栈，每一层的与将上层和下层进行通信。层之间的通信由协议定义。

Network communications requires protocols to cover high-level application communication all the way down to wire communication and the complexity handled by encapsulation in protocol layers.

网络通信需要协议涵盖高级的应用通信，一直到物理线路通信和协议层中封装的复杂处理。

### ISO OSI Protocol

ISO OSI协议

Although it was never properly implemented, the OSI (Open Systems Interconnect) protocol has been a major influence in ways of talking about and influencing distributed systems design. It is commonly given in the following figure: 

虽然它从没有清晰实现，OSI（开放系统互联）协议在分布式系统设计方面有着很大的影响力。通常如下图所示：

![iso](../assets/iso.gif)

OSI layers

OSI层

The function of each layer is:

每一层的功能：

* Network layer provides switching and routing technologies
* 网络层提供了交换和路由技术

* Transport layer provides transparent transfer of data between end systems and is responsible for end-to-end error recovery and flow control
* 传输层提供了数据的传输交换

* Session layer establishes, manages and terminates connections between applications.
* Presentation layer provides independence from differences in data representation (e.g. encryption)
* Application layer supports application and end-user processes


### TCP/IP Protocol

While the OSI model was being argued, debated, partly implemented and fought over, the DARPA internet research project was busy building the TCP/IP protocols. These have been immensely successful and have led to The Internet (with capitals). This is a much simpler stack:

![tcp_stack](../assets/tcp_stack.gif)


### Some Alternative Protocols

Although it almost seems like it, the TCP/IP protocols are not the only ones in existence and in the long run may not even be the most successful. There are many protocols occupying significant niches, such as

* Firewire
* USB
* Bluetooth
* WiFi


There is active work continuing on many other protocols, even quite bizarre ones such as those for the "internet in space."

The focus in this book will be on the TCP/IP, but you should be aware of these other ones. 
