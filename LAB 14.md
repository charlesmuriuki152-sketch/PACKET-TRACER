# 🌐 Cisco Packet Tracer: FTP Clients and Servers

## 📌 Overview

This project demonstrates how **File Transfer Protocol (FTP)** works in a computer network using Cisco Packet Tracer.

FTP allows a client to connect to a server to upload, download, and manage files over a network. In this lab, I explore FTP services, client-server communication, and file transfers.

This project is designed for networking beginners who want hands-on experience with network protocols and services.

---

## 🎬 Watch the Lab Demonstration

Click the thumbnail below to watch the video demonstration on YouTube.

[![FTP Clients and Servers | Cisco Packet Tracer](https://img.youtube.com/vi/MOtB2-n08ig/hqdefault.jpg)](https://youtu.be/MOtB2-n08ig)

▶️ **[Watch the full video on YouTube](https://youtu.be/MOtB2-n08ig)**

---

## 🎯 Lab Objectives

By completing this lab, you will learn how to:

* Understand FTP and its purpose.
* Identify the roles of an FTP client and an FTP server.
* Configure FTP services in Cisco Packet Tracer.
* Establish communication between a client and an FTP server.
* Explore file uploads and downloads.
* Understand how application-layer protocols support network communication.

---

## 🧰 Tools and Requirements

* **Cisco Packet Tracer**
* A PC configured as an FTP client
* A server configured with FTP services
* Network connections between the client and server

---

## 📂 Download the Packet Tracer Activity

Download the activity file and open it in Cisco Packet Tracer to explore the lab.

📥 **[Download Use FTP Services.pka](https://github.com/charlesmuriuki152-sketch/Packet-Tracer/blob/main/Use%20FTP%20Services.pka)**

---

## 🔍 What Is FTP?

**FTP (File Transfer Protocol)** is an application-layer protocol used to transfer files between a client and a server over a network.

For example, a user can connect to an FTP server to upload a document or download a file.

FTP traditionally uses:

* **TCP port 21:** Control connection used to send commands and receive responses.
* **TCP port 20:** Traditionally used for data transfers in active FTP. Passive FTP uses a server-selected port for the data connection.

FTP does not encrypt traffic by default, so credentials and transferred data may be exposed. Secure alternatives include **SFTP** and **FTPS**.

---

## 🖥️ FTP Client vs FTP Server

| Component    | Function                                                     |
| ------------ | ------------------------------------------------------------ |
| FTP Client   | Connects to the FTP server and requests file operations.     |
| FTP Server   | Provides FTP services and manages access to available files. |
| Network      | Carries communication between the client and server.         |
| FTP Protocol | Defines commands and responses used during file transfers.   |

### How It Works

1. The client establishes a connection to the FTP server.
2. The client provides authentication details if required.
3. The server checks the login information.
4. The client requests an operation, such as listing, uploading, or downloading files.
5. The server responds and performs the permitted operation.

---

## 🧪 Lab Procedure

Use the provided `.pka` activity and follow its instructions.

### Step 1: Open the Activity

Download `Use FTP Services.pka` and open it in Cisco Packet Tracer.

### Step 2: Inspect the Network

Identify the client, FTP server, and network connections. Check the IP addresses and ensure that the devices are correctly configured.

### Step 3: Check Connectivity

If the activity permits command-line testing, use `ping` from the client to test connectivity to the server's IP address.

### Step 4: Examine FTP Services

Open the server configuration and locate the **Services** tab. Select **FTP** and examine whether the service is enabled and which users and files are configured.

### Step 5: Connect to the FTP Server

Use the client command prompt and the FTP command supported by the activity. Enter the server's IP address and provide the configured credentials when prompted.

### Step 6: Explore File Operations

Depending on the activity configuration, try commands such as:

| FTP Command    | Purpose                                                        |
| -------------- | -------------------------------------------------------------- |
| `dir`          | Lists files and directories available through the FTP session. |
| `get filename` | Downloads a file from the server.                              |
| `put filename` | Uploads a local file to the server.                            |
| `help`         | Displays supported FTP commands.                               |
| `quit`         | Ends the FTP session.                                          |

*Available commands and file permissions depend on the FTP client and server configuration.*

---

## 🔬 Key Observations

During this lab, focus on the following concepts:

* **Client-server communication:** The client requests services, and the server responds.
* **Authentication:** The server may require a username and password.
* **File transfer:** FTP supports operations for uploading and downloading files.
* **Application-layer protocols:** FTP enables file transfer through defined commands and responses.
* **TCP:** FTP uses TCP to provide reliable transport.
* **Network connectivity:** Correct addressing and connectivity are necessary for successful communication.

---

## 🧠 What I Learned

This lab demonstrates how FTP services operate in a simulated network. It provides practical experience with client-server communication, authentication, and file transfers.

Using Cisco Packet Tracer makes it easier to explore how network services work before applying these concepts to real networking environments.

---

## 📚 Key Networking Concepts

* File Transfer Protocol (FTP)
* Client-server architecture
* Application-layer protocols
* TCP and port numbers
* IP addressing and connectivity
* Network services and authentication

---

## 🔐 Security Note

Traditional FTP does not encrypt usernames, passwords, or transferred files. For real-world file transfers involving sensitive information, use an appropriately configured secure protocol, such as **SFTP** or **FTPS**.

---

## 📁 Project File

* **Activity:** [Use FTP Services.pka](https://github.com/charlesmuriuki152-sketch/Packet-Tracer/blob/main/Use%20FTP%20Services.pka)
* **Video demonstration:** [FTP Clients and Servers — YouTube](https://youtu.be/MOtB2-n08ig)
* **Repository:** [Packet-Tracer on GitHub](https://github.com/charlesmuriuki152-sketch/Packet-Tracer)

---

## 👨‍💻 Author

Created as part of my hands-on learning journey in computer networking using Cisco Packet Tracer.

If you find this project useful, feel free to explore the activity, practice the lab, and share your feedback.

**Happy Networking! 🚀**
