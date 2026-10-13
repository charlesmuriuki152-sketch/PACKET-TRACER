# 🖧 Use the `ping` Command — Cisco Packet Tracer

![Cisco Networking](https://img.shields.io/badge/Cisco-Networking-blue?style=for-the-badge&logo=cisco)
![Packet Tracer](https://img.shields.io/badge/Tool-Packet%20Tracer-green?style=for-the-badge)

## 🎥 Video Tutorial

Click the thumbnail to watch the tutorial on YouTube.

[![Use the ping Command Tutorial](https://img.youtube.com/vi/S0Te4K1zDYI/maxresdefault.jpg)](https://www.youtube.com/watch?v=S0Te4K1zDYI)

📺 **[Watch on YouTube](https://www.youtube.com/watch?v=S0Te4K1zDYI)**

---

## 📌 Overview

The `ping` command is a networking tool used to test connectivity between devices on an IP network. It uses **Internet Control Message Protocol (ICMP)** to send Echo Request messages and receive Echo Reply messages.

In Cisco Packet Tracer, ping helps verify communication between PCs, routers, and other network devices.

## 🎯 Objectives

- Understand the purpose of the `ping` command.
- Test connectivity between network devices.
- Interpret ping results.
- Troubleshoot basic network connectivity problems.

## 💻 Basic Syntax

```text
ping <destination-IP-address>
```

**Example:**

```text
ping 192.168.1.1
```

This command tests connectivity to the device with IP address `192.168.1.1`.

## 🛠️ Procedure

1. Open the activity in Cisco Packet Tracer.
2. Select the source PC.
3. Navigate to **Desktop → Command Prompt**.
4. Enter `ping` followed by the destination IP address.
5. Press **Enter**.
6. Examine the results to determine whether the destination responds.

📂 **Activity file:** [Use the ping Command.pka](https://github.com/charlesmuriuki152-sketch/Packet-Tracer/blob/main/Use%20the%20ping%20Command.pka)

## ✅ Understanding Ping Results

**Successful response:**
```text
Reply from 192.168.1.1: bytes=32 time<1ms TTL=255
```

This indicates that the destination responded to the ping request.

**Request timed out:**
```text
Request timed out.
```

No response was received within the allowed time.

**Destination host unreachable:**

The device reporting the message cannot deliver the packet to the destination.

## 🔍 Troubleshooting

If ping fails, check the following:

- IP addresses and subnet masks.
- Default gateway configuration.
- Network cables and interface status.
- Routing configuration.
- Whether ICMP traffic is blocked.

Useful commands:

```text
ipconfig
ping <destination-IP-address>
```

On Cisco IOS devices:

```text
show ip interface brief
show ip route
```

## 🧠 Key Concepts

- **Ping:** Tests IP reachability.
- **ICMP:** Protocol used by ping.
- **IP address:** Identifies a network interface.
- **Default gateway:** Forwards traffic to other networks.
- **Packet loss:** Occurs when packets or expected responses are not received.

## 🎓 Conclusion

The `ping` command is an essential networking tool for testing connectivity and troubleshooting communication problems. Practising with Cisco Packet Tracer helps develop fundamental networking and diagnostic skills.

---

### 📂 Resources

- **[Download the Packet Tracer activity](https://github.com/charlesmuriuki152-sketch/Packet-Tracer/blob/main/Use%20the%20ping%20Command.pka)**
- **[Watch the YouTube tutorial](https://www.youtube.com/watch?v=S0Te4K1zDYI)**

<div align="center">

**Cisco Packet Tracer | Networking Fundamentals**

*Learn • Configure • Test • Troubleshoot*

</div>
