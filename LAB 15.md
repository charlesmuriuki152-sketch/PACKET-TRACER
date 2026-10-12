# 🌐 Cisco Packet Tracer: Use Telnet and SSH

## 📌 Overview

This project demonstrates how to remotely access and manage network devices using **Telnet and SSH** in Cisco Packet Tracer.

Telnet and SSH allow users to access a device's command-line interface over a network. However, SSH provides encrypted communication, while Telnet transmits data without encryption.

This lab provides hands-on experience with remote access, router configuration, and network security.

---

## 🎬 Watch the Lab Demonstration

Click the thumbnail below to watch the video tutorial on YouTube.

[![Cisco Packet Tracer: Use Telnet and SSH](https://img.youtube.com/vi/1UmEL5GtXaM/hqdefault.jpg)](https://www.youtube.com/watch?v=1UmEL5GtXaM)

▶️ **[Watch the full tutorial on YouTube](https://www.youtube.com/watch?v=1UmEL5GtXaM)**

---

## 🎯 Lab Objectives

By completing this lab, you will learn how to:

* Understand Telnet and SSH.
* Configure remote access to a Cisco router.
* Connect to a router using Telnet.
* Configure SSH for secure remote administration.
* Understand the security differences between Telnet and SSH.
* Identify the default TCP ports used by both protocols.
* Test remote connectivity in Cisco Packet Tracer.

---

## 🧰 Tools and Requirements

* Cisco Packet Tracer
* A Cisco router
* A PC or client device
* Appropriate network connections
* IP addressing configured for connectivity

---

## 📂 Download the Packet Tracer Activity

Download the activity file and open it in Cisco Packet Tracer to practise the lab.

📥 **[Download Use Telnet and SSH.pka](https://github.com/charlesmuriuki152-sketch/Packet-Tracer/blob/main/Use%20Telnet%20and%20SSH.pka)**

---

## 🔍 What Is Telnet?

**Telnet** is a network protocol that allows remote access to a device's command-line interface.

* Uses TCP port **23** by default.
* Allows users to manage remote devices.
* Does not encrypt transmitted data.
* Is generally unsuitable for secure remote administration over untrusted networks.

## 🔐 What Is SSH?

**SSH (Secure Shell)** is a protocol used to securely access and manage remote devices over a network.

* Uses TCP port **22** by default.
* Encrypts communications.
* Helps protect credentials and commands from being read by someone capturing network traffic.
* Is preferred over Telnet for remote device administration.

---

## ⚖️ Telnet vs SSH

| Feature                        | Telnet                     | SSH                             |
| ------------------------------ | -------------------------- | ------------------------------- |
| Full name                      | Teletype Network           | Secure Shell                    |
| Default TCP port               | 23                         | 22                              |
| Remote command-line access     | Yes                        | Yes                             |
| Encrypts communication         | No                         | Yes                             |
| Security                       | Insecure for sensitive use | Secure when properly configured |
| Recommended for administration | Generally no               | Yes                             |

---

## 🧪 Lab Procedure

Follow the instructions in the provided Packet Tracer activity.

### Step 1: Open the Activity

Download `Use Telnet and SSH.pka` and open it in Cisco Packet Tracer.

### Step 2: Examine the Network

Identify the PC, router, and network connections. Check the device IP addresses and interface status.

### Step 3: Test Connectivity

From the PC's command prompt, use `ping` to test connectivity to the router's IP address, if supported by the activity.

### Step 4: Explore Telnet

Connect to the router using Telnet if it is configured and enabled. Observe how the remote command-line session works.

### Step 5: Explore SSH

Connect to the router using SSH after the required SSH configuration has been completed. Observe how SSH provides encrypted remote access.

### Step 6: Compare the Protocols

Compare the connection process and security properties of Telnet and SSH.

---

## 🔬 Key Networking Concepts

* **Remote access:** Managing a network device from another computer.
* **Client and server:** The client initiates a connection to the remote device.
* **TCP:** Provides reliable transport for Telnet and SSH.
* **Port numbers:** Identify the services to which clients connect.
* **Encryption:** SSH protects data in transit.
* **Network configuration:** Correct IP addressing and connectivity are necessary for remote access.

---

## 🧠 What I Learned

This lab demonstrates how remote access protocols allow network administrators to manage devices without being physically connected to their console ports.

It also highlights why SSH is preferred over Telnet: SSH encrypts communication, while Telnet does not.

Cisco Packet Tracer provides a practical environment for learning these concepts and practising router administration.

---

## 🔐 Security Note

Telnet transmits data without encryption and should not be used for sensitive administration across untrusted networks. For real-world device management, use SSH with strong authentication and appropriate security settings.

---

## 📁 Project Resources

* **Packet Tracer Activity:** [Use Telnet and SSH.pka](https://github.com/charlesmuriuki152-sketch/Packet-Tracer/blob/main/Use%20Telnet%20and%20SSH.pka)
* **YouTube Tutorial:** [Watch Use Telnet and SSH](https://www.youtube.com/watch?v=1UmEL5GtXaM)
  

---

## 👨‍💻 Author

Created as part of my hands-on learning journey in computer networking using Cisco Packet Tracer.

Feel free to explore the activity, practise the lab, and share feedback.

**Happy Networking! 🚀**
