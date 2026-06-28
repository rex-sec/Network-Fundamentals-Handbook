  # Network-Fundamentals-Handbook]
## 1. What is Network?
Netorking is the process of connecting two and more devices each other. So they can communicate and share data with each other. 

## What is Internet?
The Internet is a global network of interconnected network that allows device that allow device worldwide to communicate and share information.

## IP Address (Internet Protocol)
An IP address is a unique logical address assign to a device for communicate on network. 

## MAC Address (Media Access Control)
A MAC is a unique physical address assign to a netrwork interface by the Manufacturer.

## What is Ping?
Ping is a network Utility used to test Connectivity beetween two devices.
### How it works:
It sends a small packet called **ICMP Echo Request** to the target device. If the device is active, it sends back an **ICMP Echo Reply**

### 📊 Network Connection Diagram (Ping Process)

```
  [ Your PC ]  ---------------------------->  [ Google Server ]
                 ICMP Echo Request (Are you alive?)

  [ Your PC ]  <----------------------------  [ Google Server ]
                 ICMP Echo Reply (Yes, I am alive!)
```

### Command Syntax:
`ping <IP_Address_or_Domain>`

### Examples:
* `ping 8.8.8.8`
* `ping google.com`

## LAN Topologies
A LAN Topology is the physical or logical layout of devices in a local area network.

- 1.Star Topology
Star topology is a network topology in which all devices are connected to central swich or Hub.

- 2.Bus Topology
bus topology is a network topology in which all devices are connected to a single backbone cable.

- 3.Ring Topology
Ring topology is a network topology in which each device is connected to two other devices. forming and circular.


## What is Swich? 
Swich is a networking device that connect multipal Devices with a local area network . Work in layer 2 use MAC address.

## What is Router?
A router is a layer 3 networking device that connect diffrent network using  IP address . its connect your (LAN) to internet.


## Subnetting 
Subnetting is a process of dividing one large network into multipal smaller networks its calls subnets.

## ARP (Address Resolution Protocol)
ARP is a protocol used to resolve an IP Address into MAC Address on a LAN.

###  ARP Process Diagram

```
1. ARP REQUEST (Broadcast - Subse Poochna)
----------------------------------------------------------------------
[ Your PC ] ------------------> "Who has IP 192.168.1.5? Tell me!"
(IP: 192.168.1.1)    |
                     |--------> [ Device B (192.168.1.2) ] -> "Not me."
                     |--------> [ Device C (192.168.1.5) ] -> "Hey, that's me!"


2. ARP REPLY (Unicast - Sirf Target ka Jawab Dena)
----------------------------------------------------------------------
[ Your PC ] <------------------ "I have 192.168.1.5! My MAC is AA:BB:CC:DD..."
                     |
                     x [ Device C (192.168.1.5) ]
```

## DHCP (Dynamic Host Configuration Protocol)?
DHCP protocol is a network protocol that automatically assign an IP Address.

### The DORA Process Diagram

Jab aapka device Wi-Fi se connect hota hai, toh wo DHCP Server ke sath 4 steps me baat karta hai (D-O-R-A):

```
   [ Your PC (Client) ]                     [ Wi-Fi Router (DHCP Server) ]
            |                                             |
            | ------------ DISCOVER (Broadcast) --------> |
            |   "Hey, I am new here! Who can give IP?"   |
            |                                             |
            | <----------- OFFER (Unicast) -------------- |
            |   "I have an IP for you: 192.168.1.50"      |
            |                                             |
            | ------------ REQUEST (Broadcast) ---------> |
            |   "Great! Please lock 192.168.1.50 for me." |
            |                                             |
            | <----------- ACKNOWLEDGE (Unicast) -------- |
            |   "Done! You can use it now for 24 hours."  |
            v                                             v
```
   protocol--> UDP |  Server port--> 67  |   Client port--> 68


