# Cisco Packet Tracer: Identify MAC and IP Addresses (ARP)

## 📌 Project Overview

This project explores how the **Address Resolution Protocol (ARP)** operates in local and remote network communication using Cisco Packet Tracer.

The lab demonstrates how devices determine the MAC address associated with an IPv4 address and how ARP works when communicating with a device on the same local area network (LAN) versus a device on a remote network.

Using Simulation Mode, I examined ARP requests and replies, ICMP packets, Ethernet frames, and IP addressing to understand how data travels between devices.

## 🎯 Objectives

* Understand the purpose of ARP in IPv4 networks.
* Observe ARP requests and replies in Cisco Packet Tracer.
* Identify source and destination MAC addresses in Ethernet frames.
* Identify source and destination IPv4 addresses in IP packets.
* Compare ARP behavior during local and remote network communication.
* Understand the role of the default gateway when accessing remote networks.
* Use Simulation Mode to inspect PDUs and analyze network traffic.

## 🛠️ Tools and Technologies

* **Cisco Packet Tracer** — Network simulation.
* **ARP (Address Resolution Protocol)** — Resolves IPv4 addresses to MAC addresses on a local network.
* **IPv4** — Logical addressing at OSI Layer 3.
* **Ethernet** — Local network communication at OSI Layer 2.
* **ICMP** — Connectivity testing using `ping`.
* **OSI Model** — Understanding network communication layers.

## 🧪 Part 1: ARP Between Devices on the Same LAN

### Scenario

Two devices communicate within the same local network:

* **Source IP:** `172.16.31.3`
* **Destination IP:** `172.16.31.2`

Before the source device can send an Ethernet frame to the destination, it needs to know the destination device's MAC address. If that mapping is not already in its ARP cache, the source broadcasts an ARP request on the local network.

### Procedure

1. Opened the Packet Tracer topology.

2. Accessed the command prompt on host `172.16.31.3`.

3. Entered the following command:

   ```bash
   ping 172.16.31.2
   ```

4. Switched to Simulation Mode.

5. Repeated the ping command to generate network traffic.

6. Observed the ARP request broadcast on the local network.

7. Inspected the ARP reply sent by the destination device.

8. Examined the MAC and IP addresses in the PDU details.

9. Used Capture / Forward to follow the packets through the network.

### Initial PDU Information

| Field                   | Value            |
| ----------------------- | ---------------- |
| Source Device IP        | `172.16.31.3`    |
| Source MAC Address      | `0060.7036.2849` |
| Destination Device IP   | `172.16.31.2`    |
| Destination MAC Address | `000C.85CC.1DA7` |

### ARP Behavior on a Local Network

When the destination is on the same subnet:

1. The source checks its ARP cache for the destination's MAC address.
2. If no mapping exists, it broadcasts an ARP request asking which device owns the destination IPv4 address.
3. The device with the matching IPv4 address responds with an ARP reply containing its MAC address.
4. The source caches the mapping and sends the Ethernet frame directly to the destination.

**Key observation:** ARP resolves the destination's IPv4 address to its MAC address, allowing the source to deliver Ethernet frames directly to the destination on the local network.

## 🌐 Part 2: ARP When Communicating with a Remote Network

### Scenario

When a device communicates with an IPv4 address outside its local subnet, it does not use ARP to discover the remote host's MAC address.

Instead, the source resolves the MAC address of its **default gateway**.

### Procedure

1. Generated traffic toward a device on a remote network.
2. Switched to Simulation Mode.
3. Observed ARP activity associated with forwarding traffic to the default gateway.
4. Inspected the Ethernet frame and IPv4 packet headers.
5. Followed the PDU as it passed through the router.
6. Compared the MAC and IP addresses at different points along the path.

### ARP Behavior on a Remote Network

When the destination is on a different subnet:

1. The source determines that the destination IP address is outside its local subnet.
2. The source checks its ARP cache for the default gateway's MAC address.
3. If the mapping is unknown, the source broadcasts an ARP request on its local LAN to resolve the gateway's IPv4 address.
4. The router responds with its local interface's MAC address.
5. The source sends the Ethernet frame to the router, while the IP packet retains the remote destination's IPv4 address.
6. The router examines the destination IP address and forwards the packet toward the remote network.
7. If necessary, the router uses ARP on the outgoing network to resolve the next-hop IPv4 address to a MAC address.

### Addressing Differences

| Address Type      | Same LAN                          | Remote Network                                      |
| ----------------- | --------------------------------- | --------------------------------------------------- |
| Destination IP    | Destination host's IP             | Remote host's IP                                    |
| Destination MAC   | Destination host's MAC            | Default gateway's MAC on the source LAN             |
| ARP target        | Destination host                  | Default gateway                                     |
| Ethernet delivery | Direct to destination             | To the next-hop router                              |
| Default gateway   | Not needed for this communication | Required for communication outside the local subnet |

**Important:** IP addresses generally remain the same from source to destination, assuming no NAT occurs. Ethernet MAC addresses change at each routed hop because each Ethernet frame is addressed to the next hop on the corresponding network segment.

## 📚 Key Concepts Learned

### 1. Address Resolution Protocol (ARP)

ARP maps a known IPv4 address to a MAC address on the local network. It enables a device to build the Ethernet frame required for local delivery.

### 2. ARP Request

An ARP request is normally sent as an Ethernet broadcast when the required IP-to-MAC mapping is not already available in the ARP cache.

### 3. ARP Reply

An ARP reply provides the MAC address associated with the requested IPv4 address.

### 4. Local Network Communication

For devices on the same subnet, the source resolves the destination host's MAC address and sends the Ethernet frame directly to that host.

### 5. Remote Network Communication

For remote destinations, the source resolves the MAC address of its default gateway rather than the MAC address of the remote host.

### 6. MAC Address vs. IP Address

* **MAC address:** Used for local Ethernet frame delivery.
* **IP address:** Used for logical addressing and routing between networks.

### 7. Simulation Mode

Packet Tracer Simulation Mode helps visualize ARP requests, ARP replies, ICMP messages, Ethernet frames, and IP packets as they move through the network.

## 📁 Repository Contents

| File                                | Description                                                                 |
| ----------------------------------- | --------------------------------------------------------------------------- |
| `Identify-MAC-and-IP-Addresses.pkt` | Cisco Packet Tracer lab file                                                |
| `README.md`                         | Documentation of the lab objectives, ARP behavior, procedures, and findings |

*Replace the `.pkt` filename above if your actual file has a different name.*

## ✅ Conclusion

This lab demonstrates how ARP supports IPv4 communication by resolving IP addresses to MAC addresses on local network segments.

For communication between devices on the same LAN, ARP resolves the destination host's MAC address. For communication with a remote network, ARP resolves the default gateway's MAC address so the source can forward the Ethernet frame to the router.

By inspecting PDUs in Cisco Packet Tracer, I explored the relationship between ARP, Ethernet addressing, IPv4 addressing, and routing.

## 💡 Skills Demonstrated

* ARP request and reply analysis
* MAC address identification
* IPv4 addressing
* Local and remote network communication
* Ethernet frame inspection
* ICMP connectivity testing
* Default gateway operation
* Cisco Packet Tracer simulation
* Networking fundamentals

---

**Lab:** Identify MAC and IP Addresses
**Focus:** ARP on Local and Remote Networks
**Platform:** Cisco Packet Tracer
**Category:** Networking Fundamentals
