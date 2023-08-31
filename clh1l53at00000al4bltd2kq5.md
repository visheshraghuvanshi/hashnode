---
title: "MAC Sub layer"
datePublished: Sat Apr 29 2023 06:12:01 GMT+0000 (Coordinated Universal Time)
cuid: clh1l53at00000al4bltd2kq5
slug: cn-mac-sublayer
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682698042446/2fa76f2a-6acc-4ecf-8dcd-ef5c9cca4cef.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1682748711930/0a9f97a2-27d2-477f-9551-d9fd93973d03.png

---

## MAC Sub layer

The Media Access Control (MAC) sublayer is one of two sublayers that make up the Data Link Layer in the OSI model of computer networking. The MAC sublayer is responsible for controlling how devices on a network access and use the physical network medium.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682747896715/5d442406-1856-4597-b8eb-566ceb1920f3.jpeg align="center")

Here are some key features and functions of the MAC sublayer:

1. **MAC addresses:** The MAC sublayer uses MAC addresses to uniquely identify devices on a network. MAC addresses are 48-bit identifiers that are assigned by the manufacturer of a network interface card (NIC). The MAC sublayer is responsible for ensuring that each device on the network has a unique MAC address.
    
2. **Framing:** The MAC sublayer is responsible for adding a header and trailer to data packets received from the network layer above it. This process is called framing. The header includes information such as the source and destination MAC addresses, while the trailer includes a cyclic redundancy check (CRC) value that is used to check for transmission errors.
    
3. **Media access control:** The MAC sublayer is responsible for controlling how devices access the network medium. This is typically done using a media access control protocol, such as Carrier Sense Multiple Access with Collision Detection (CSMA/CD) or Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA). These protocols help to avoid collisions on the network medium by ensuring that only one device transmits data at a time.
    
4. **Error detection and correction:** The MAC sublayer is responsible for detecting and correcting errors in data transmissions. This is done using the CRC value included in the frame trailer. If the CRC value does not match the calculated value at the receiving device, the frame is discarded.
    
5. **MAC sublayer protocols:** Several MAC sublayer protocols are used in different types of networks. For example, Ethernet is a widely used MAC protocol that uses CSMA/CD to control access to the network medium. Other MAC protocols include Token Ring, which uses a token-passing mechanism to control access, and Wi-Fi, which uses CSMA/CA to control access to the wireless medium.
    

### MAC Addressing

The MAC sublayer uses MAC addresses to uniquely identify devices on a network. MAC addresses are 48-bit identifiers that are assigned by the manufacturer of a network interface card (NIC).

Here are some important points to understand about MAC addressing:

1. **Format:** MAC addresses are usually represented as a string of 12 hexadecimal digits (0-9 and A-F), separated by colons or hyphens. For example, 00:1a:2b:3c:4d:5e.
    
2. **Unique identification:** Each device on a network must have a unique MAC address. This is important because the MAC address is used by the MAC sublayer to determine where to send data packets.
    
3. **MAC address table:** When a device on a network sends a data packet, the MAC sublayer looks up the destination MAC address in a MAC address table. This table contains a list of MAC addresses and the corresponding ports on the network switch where the devices are connected.
    
4. **Broadcast addresses:** A broadcast address is a special MAC address that is used to send a data packet to all devices on a network. The broadcast address is FF:FF:FF:FF:FF:FF.
    
5. **Multicast addresses:** A multicast address is a special MAC address that is used to send a data packet to a group of devices on a network. Multicast addresses begin with a specific prefix (01-09-5E) and are used in protocols such as Internet Group Management Protocol (IGMP).
    
6. **MAC address spoofing:** MAC address spoofing is the practice of changing the MAC address of a device. This can be used to bypass security measures that are based on MAC addresses. However, MAC address spoofing is not a reliable way to hide a device on a network, as it can be detected using other techniques such as port security.
    

### Binary Exponential Back-off (BEB) Algorithm

The Binary Exponential Back-off (BEB) algorithm is a collision resolution mechanism used in Ethernet networks. It is used when two or more devices try to transmit data simultaneously on the same network segment, resulting in a collision.

Here are the basic steps of the BEB algorithm:

1. When a device detects a collision, it stops transmitting and waits for a random period of time before trying to transmit again. The initial waiting time is chosen randomly from a range of values.
    
2. If the transmission is successful, the device resumes normal operation.
    
3. If the transmission is unsuccessful due to another collision, the device doubles the waiting time and chooses a new random value from the range.
    
4. The device repeats step 3 until it reaches a maximum number of retries, after which it gives up and reports the failure to higher layers.
    

Here are some key points to understand about the BEB algorithm:

1. The purpose of the algorithm is to reduce the probability of collisions and improve network performance by regulating access to the network medium.
    
2. The range of waiting times and the maximum number of retries are defined by the network standard. For example, in Ethernet networks, the range of waiting times is 0 to (2^n - 1) x 512-bit times, where n is the number of failed attempts, and the maximum number of retries is typically 16.
    
3. The BEB algorithm is a type of exponential back-off algorithm, meaning that the waiting time increases exponentially with each failed attempt. This helps to reduce the likelihood of multiple devices retrying at the same time, which could result in another collision.
    
4. The BEB algorithm is a simple and effective collision resolution mechanism, but it can lead to long delays and reduced network performance if collisions are frequent. For this reason, many modern networks use other mechanisms, such as Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA), to reduce the likelihood of collisions.
    

## Distributed Random Access Schemes/Contention Schemes

Distributed random access schemes, also known as contention schemes, are a type of multiple-access protocol that allows multiple nodes to share a communication channel without central coordination. These schemes are used in a variety of networks, including wireless networks, local area networks (LANs), and metropolitan area networks (MANs).

### Data Services (ALOHA and Slotted ALOHA)

Distributed random access schemes are used in data communication networks to regulate access to the communication medium when multiple devices are competing to transmit data. Two of the earliest and most widely used distributed random access schemes are ALOHA and slotted ALOHA.

1. ALOHA: ALOHA is a simple, unslotted distributed random access scheme that was developed in the late 1960s for satellite communication networks. In ALOHA, devices transmit data whenever they have data to send, without checking whether the medium is busy. If a collision occurs, devices stop transmitting for a random time period and then try to retransmit. ALOHA has a high collision probability, which limits its performance. However, it is simple and does not require synchronization between devices.
    
    ![Difference between Pure aloha and Slotted aloha - javatpoint](https://static.javatpoint.com/difference/images/pure-aloha-vs-slotted-aloha.png align="left")
    
2. Slotted ALOHA: Slotted ALOHA is an improvement over ALOHA that was developed to reduce collision probability. In slotted ALOHA, the communication medium is divided into time slots, and devices transmit data only at the beginning of a time slot. If a collision occurs, devices stop transmitting and wait for the next time slot before retransmitting. Slotted ALOHA has a lower collision probability than ALOHA, but requires synchronization between devices.
    
    ![Difference between Pure aloha and Slotted aloha - javatpoint](https://static.javatpoint.com/difference/images/pure-aloha-vs-slotted-aloha2.png align="left")
    

Here are some key points to understand about ALOHA and slotted ALOHA:

1. ALOHA and slotted ALOHA are simple, distributed random access schemes that do not require a central authority to regulate access to the communication medium.
    
2. ALOHA and slotted ALOHA have a higher collision probability than other distributed random access schemes, which limits their performance.
    
3. ALOHA and slotted ALOHA are often used as building blocks for more advanced distributed random access schemes, such as CSMA and CSMA/CD.
    
4. ALOHA and slotted ALOHA are particularly useful in networks with low traffic loads or intermittent traffic, such as sensor networks or machine-to-machine networks.
    

### Local-Area Networks (CSMA, CSMA/CD, CSMA/CA)

**CSMA**

CSMA stands for Carrier Sense Multiple Access. In CSMA, nodes listen to the channel before transmitting. If the channel is busy, the node waits until the channel is idle before transmitting.

Here are the steps involved in CSMA:

1. A node wants to transmit data.
    
2. The node listens to the channel.
    
3. If the channel is busy, the node waits.
    
4. If the channel is idle, the node transmits its data.
    
    ![Carrier Sense Multiple Access (CSMA) - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/11-19.png align="left")
    

**CSMA/CD**

CSMA/CD stands for Carrier Sense Multiple Access with Collision Detection. CSMA/CD is a variation of CSMA that detects collisions. In CSMA/CD, if two nodes start transmitting at the same time, they both detect the collision and stop transmitting.

![](https://media.geeksforgeeks.org/wp-content/uploads/22-8.png align="left")

Here are the steps involved in CSMA/CD:

1. A node wants to transmit data.
    
2. The node listens to the channel.
    
3. If the channel is busy, the node waits.
    
4. If the channel is idle, the node starts transmitting.
    
5. While transmitting, the node listens to the channel.
    
6. If the node detects a collision, it stops transmitting.
    
7. The node waits for a random amount of time before trying to transmit again.
    

![](https://media.geeksforgeeks.org/wp-content/uploads/33-1-2.png align="left")

**CSMA/CA**

CSMA/CA stands for Carrier Sense Multiple Access with Collision Avoidance. CSMA/CA is a variation of CSMA that avoids collisions by having nodes wait a random amount of time before transmitting. This ensures that two nodes will not start transmitting at the same time, even if they both hear the channel is idle.

Here are the steps involved in CSMA/CA:

1. A node wants to transmit data.
    
2. The node listens to the channel.
    
3. If the channel is busy, the node waits.
    
4. If the channel is idle, the node waits for a random amount of time before transmitting.
    
5. The node starts transmitting.
    

![Lightbox](https://media.geeksforgeeks.org/wp-content/uploads/20200420165042/article9.png align="left")

## Collision Free Protocols

Collision-free protocols are a type of multiple-access protocol that allows multiple nodes to share a communication channel without collisions. Collisions occur when two nodes transmit at the same time, and they can corrupt the data that is being transmitted. Collision-free protocols are designed to prevent collisions from occurring, and they are often used in networks where collisions can be costly or disruptive.

There are several different collision-free protocols, each with its own advantages and disadvantages. Some of the most common collision-free protocols include:

### Basic Bit Map

A bit-map protocol is a collision-free protocol that is used in local area networks (LANs). In a bit-map protocol, each node is assigned a unique bit in a bitmap. When a node wants to transmit, it sets its bit in the bitmap. The other nodes listen to the bitmap and wait until all of the bits are clear before transmitting.

Here is an example of how a bit-map protocol works:

1. There are 5 nodes in a LAN.
    
2. Each node is assigned a unique bit in a bitmap, with bit 0 being assigned to node 1, bit 1 being assigned to node 2, and so on.
    
3. Node 1 wants to transmit.
    
4. Node 1 sets its bit in the bitmap.
    
5. The other nodes listen to the bitmap and see that bit 0 is set.
    
6. The other nodes wait for bit 0 to clear before transmitting.
    
7. Once bit 0 has cleared, the other nodes can transmit.
    

![Collision-Free Protocols in Computer Network - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20230222150516/bmp1.png align="left")

Bit-map protocols are a simple and efficient way to prevent collisions in LANs. They are also easy to implement and require little hardware.

Here are some of the advantages of bit-map protocols:

* They are simple and easy to implement.
    
* They require little hardware.
    
* They are efficient in terms of bandwidth usage.
    

Here are some of the disadvantages of bit-map protocols:

* They can be susceptible to collisions if the number of nodes in the network is large.
    
* They can be inefficient in terms of latency, as nodes must wait for all of the bits in the bitmap to clear before transmitting.
    

### BRAP

BRAP, or Binary Recursive Allocation Protocol, is a collision-free protocol that is used in local area networks (LANs). BRAP is a variation of the bit-map protocol, and it is more efficient in terms of latency.

In BRAP, each node is assigned a unique binary number. When a node wants to transmit, it starts counting down from its number. The other nodes listen to the countdown and wait until all of the nodes have reached zero before transmitting.

Here is an example of how BRAP works:

1. There are 5 nodes in a LAN.
    
2. Each node is assigned a unique binary number, with node 1 being assigned the number 0000, node 2 being assigned the number 0001, and so on.
    
3. Node 1 wants to transmit.
    
4. Node 1 starts counting down from 0000.
    
5. The other nodes listen to the countdown and see that node 1 is counting down.
    
6. The other nodes wait for node 1 to reach zero before transmitting.
    
7. Once node 1 has reached zero, the other nodes can transmit.
    

BRAP is a more efficient collision-free protocol than the bit-map protocol. It is more efficient in terms of latency, as nodes do not have to wait for all of the bits in the bitmap to clear before transmitting.

Here are some of the advantages of BRAP:

* It is more efficient in terms of latency than the bit-map protocol.
    
* It is simple and easy to implement.
    
* It requires little hardware.
    

Here are some of the disadvantages of BRAP:

* It can be susceptible to collisions if the number of nodes in the network is large.
    
* It can be less efficient in terms of bandwidth usage than the bit-map protocol.
    

### Binary Count Down

The binary countdown is a collision-free protocol that is used in local area networks (LANs). In binary countdown, each node is assigned a unique binary number. When a node wants to transmit, it starts counting down from its number. The other nodes listen to the countdown and wait until all of the nodes have reached zero before transmitting.

Here is an example of how binary countdown works:

1. There are 5 nodes in a LAN.
    
2. Each node is assigned a unique binary number, with node 1 being assigned the number 0000, node 2 being assigned the number 0001, and so on.
    
3. Node 1 wants to transmit.
    
4. Node 1 starts counting down from 0000.
    
5. The other nodes listen to the countdown and see that node 1 is counting down.
    
6. The other nodes wait for node 1 to reach zero before transmitting.
    
7. Once node 1 has reached zero, the other nodes can transmit.
    

Binary countdown is a more efficient collision-free protocol than the bit-map protocol. It is more efficient in terms of latency, as nodes do not have to wait for all of the bits in the bitmap to clear before transmitting.

![Collision-Free Protocols in Computer Network - GeeksforGeeks](https://media.geeksforgeeks.org/wp-content/uploads/20190319140031/binary-countdown-1.png align="left")

Here are some of the advantages of binary countdown:

* It is more efficient in terms of latency than the bit-map protocol.
    
* It is simple and easy to implement.
    
* It requires little hardware.
    

Here are some of the disadvantages of binary countdown:

* It can be susceptible to collisions if the number of nodes in the network is large.
    
* It can be less efficient in terms of bandwidth usage than the bit-map protocol.
    

Binary countdown is a good choice for networks with a small number of nodes. It is also a good choice for networks where latency is important, such as real-time applications.

## MLMA Limited Contention Protocols

MLMA Limited Contention Protocols (MLMA-LCP) are a family of collision-free media access control (MAC) protocols that are designed for wireless networks. MLMA-LCP protocols divide the nodes into groups, and each group is assigned a unique time slot. When a node wants to transmit, it waits for its assigned time slot and then transmits. If there is no collision, the node successfully transmits its packet. If there is a collision, the node waits for a random amount of time before trying again.

MLMA-LCP protocols are a good choice for wireless networks because they are efficient in terms of bandwidth usage and latency. They are also relatively easy to implement.

Here are some of the advantages of MLMA-LCP protocols:

* They are efficient in terms of bandwidth usage.
    
* They are efficient in terms of latency.
    
* They are relatively easy to implement.
    

Here are some of the disadvantages of MLMA-LCP protocols:

* They can be susceptible to collisions if the number of nodes in the network is large.
    
* They can be less efficient in terms of throughput than contention-based protocols.
    

### Adaptive Tree Walk

Adaptive Tree Walk (ATW) is a collision-free medium access control (MAC) protocol that is designed for wireless networks. ATW is a variation of the binary countdown protocol, and it is more efficient in terms of latency and throughput.

In ATW, each node is assigned a unique binary number. When a node wants to transmit, it starts counting down from its number. However, if the node hears another node counting down at the same time, it backs off and tries again later. This ensures that two nodes will not start transmitting at the same time, even if they both hear the channel is idle.

Here is an example of how ATW works:

1. There are 5 nodes in a wireless network.
    
2. Each node is assigned a unique binary number, with node 1 being assigned the number 0000, node 2 being assigned the number 0001, and so on.
    
3. Node 1 wants to transmit.
    
4. Node 1 starts counting down from 0000.
    
5. Node 2 also wants to transmit.
    
6. Node 2 starts counting down from 0001.
    
7. Node 1 hears node 2 counting down.
    
8. Node 1 backs off and tries again later.
    
9. Node 2 continues counting down.
    
10. Node 2 reaches zero and successfully transmits its packet.
    
11. Node 1 tries again and successfully transmits its packet.
    

![](https://media.geeksforgeeks.org/wp-content/uploads/20190319151547/adaptive-tree-walk.png align="left")

ATW is a more efficient collision-free protocol than the binary countdown protocol. It is more efficient in terms of latency and throughput, as nodes do not have to wait for all of the nodes to reach zero before transmitting.

Here are some of the advantages of ATW:

* It is more efficient in terms of latency and throughput than the binary countdown protocol.
    
* It is simple and easy to implement.
    
* It requires little hardware.
    

Here are some of the disadvantages of ATW:

* It can be susceptible to collisions if the number of nodes in the network is large.
    
* It can be less efficient in terms of bandwidth usage than the bit-map protocol.
    

### Performance Measuring Metrics

Performance measuring metrics are quantitative ways to measure the performance of a system or process. They can be used to track the progress of a project, identify areas for improvement, and compare the performance of different systems or processes.

There are many different performance measuring metrics that can be used, depending on the specific system or process being measured. Some common metrics include:

* **Throughput:** The amount of work that a system or process can complete in a given amount of time.
    
* **Latency:** The amount of time it takes for a system or process to respond to a request.
    
* **Error rate:** The percentage of requests that are not successful.
    
* **Reliability:** The likelihood that a system or process will perform as expected.
    
* **Availability:** The percentage of time that a system or process is available for use.
    

## IEEE Standards 802 series & their variants

IEEE 802 is a family of technical standards for local area networks (LANs) and metropolitan area networks (MANs). It is developed and maintained by the Institute of Electrical and Electronics Engineers (IEEE) LAN/MAN Standards Committee (LMSC). The IEEE 802 standards define the physical and data link layer specifications for a variety of network technologies, including Ethernet, Wi-Fi, and Bluetooth.

The IEEE 802 standards are divided into several subseries, each of which specifies a different type of network technology. The most common subseries are:

* **802.3:** Ethernet
    
* **802.11:** Wi-Fi
    
* **802.15:** Bluetooth
    
* **802.16:** WiMAX
    
* **802.20:** Mobile WiMAX
    

Each subseries is further divided into several numbered standards, each of which specifies a different aspect of the network technology. For example, the IEEE 802.3 standard is divided into the following standards:

* **802.3:** Basic Ethernet
    
* **802.3a:** Fast Ethernet
    
* **802.3ab:** Gigabit Ethernet
    
* **802.3ac:** 10 Gigabit Ethernet
    
* **802.3ad:** 40 Gigabit Ethernet
    
* **802.3ae:** 100 Gigabit Ethernet
    

**EEE 802.3:** Ethernet

Ethernet is a wired local area network (LAN) technology that is widely used in enterprise networks, home networks, and mobile networks. It is based on the Carrier Sense Multiple Access with Collision Detection (CSMA/CD) protocol, which allows multiple devices to share a single network medium without causing collisions.

**IEEE 802.11:** Wi-Fi

Wi-Fi is a wireless local area network (WLAN) technology that is widely used in home networks, enterprise networks, and mobile networks. It is based on the IEEE 802.11 family of standards, which specify the physical and data link layer specifications for wireless networks.

**IEEE 802.15:** Bluetooth

Bluetooth is a short-range wireless technology that is used for personal area networks (PANs). It is used to connect devices such as smartphones, laptops, and headsets. Bluetooth is based on the IEEE 802.15 family of standards, which specify the physical and data link layer specifications for Bluetooth networks.

**IEEE 802.16:** WiMAX

WiMAX is a metropolitan area network (MAN) technology that is used to provide broadband wireless access. It is based on the IEEE 802.16 family of standards, which specify the physical and data link layer specifications for WiMAX networks.

**IEEE 802.20:** Mobile WiMAX

Mobile WiMAX is a mobile broadband wireless technology that is used to provide high-speed Internet access to mobile devices. It is based on the IEEE 802.16 family of standards, which specify the physical and data link layer specifications for Mobile WiMAX networks.