# **Experiment: Basic Linux Data Networking Commands**

## **Aim**
To study and execute basic data networking commands in Linux using the command line interface.

---

## **Objectives**
- To understand Linux network configuration.
- To test network connectivity.
- To diagnose network-related issues.
- To access and transfer data between systems using networking tools.

---

## **Requirements**
- Linux Operating System (Ubuntu/Debian/Fedora/Kali etc.)
- Terminal access
- Basic knowledge of Linux commands
- Internet connection (optional)

---

## **Theory**
Data networking in Linux is performed using built-in terminal commands. These commands help configure systems, test connections, and troubleshoot network problems.

| Command | Purpose |
|----------|---------|
| `ifconfig` / `ip addr` | Shows network interface configuration |
| `ping` | Tests connectivity to another host |
| `hostname` | Displays system hostname |
| `traceroute` | Shows the route packets take |
| `netstat` | Displays active connections |
| `nslookup` | Queries DNS information |
| `ssh` | Secure remote login |
| `scp` | Secure file transfer |

---

## **Procedure**

### **Step 1: View IP Address and Network Interfaces**
```bash
ip addr show
```
![image1](images/image1.png)

### **Step 2:Display hostname**
```bash
hostname
```
![image2](images/image2.png)

### **step 3:Test Network connectivity(ping)**
```bash
ping google.com -c 4
```
![iamge3](images/image3.png)

### **Step 4: Trace Route to Remote Host**
```bash
traceroute google.com
```
### **Step 5: View Active Network Ports**
```bash
netstat -tulnp
```
### **Step 6: DNS Lookup**
```bash
nslookup google.com
```

### **Step 7: Remote Login using SSH**
```bash
ssh user@192.168.1.10
```
### **Step 8: File Transfer using SCP**
```bash
scp test.txt user@192.168.1.10:/home/user/
```
![image4](images/image4.png)
![image5](images/image5.png)
![image6](images/image6.png)

## **Output / Observations**

| Command     | Result                                      |
|-------------|---------------------------------------------|
| `ip addr`   | Lists network interfaces and IP addresses   |
| `ping`      | Replies received indicate connectivity      |
| `traceroute`| Displays the route path to the destination  |
| `nslookup`  | Shows DNS IP information                    |
| `ssh`       | Connects to a remote machine securely       |
| `scp`       | Transfers files securely over SSH           |

---

## **Result**
Basic Linux networking commands were successfully executed and network connectivity and configuration were verified.

---

## **Conclusion**
Linux provides powerful built-in commands for networking tasks such as configuration, troubleshooting, monitoring, and secure communication between systems.

---

## **Viva Questions**

### ❓ What is the purpose of the `ping` command?

### ✨The `ping` command is used to test network connectivity between the source and a destination host. It sends ICMP Echo Request packets and waits for Echo Reply packets to verify whether the destination is reachable and to measure round-trip time.

---

### ❓ What is the difference between SSH and Telnet?

### ✨| Feature | SSH (Secure Shell) | Telnet |
|----------|-------------------|--------|
| Security | Encrypted communication | No encryption |
| Default Port | 22 | 23 |
| Usage | Secure remote login | Unsecure remote login |
| Current Status | Widely used | Mostly outdated |

*SSH is preferred over Telnet because it provides secure communication.*

---

### ❓ How does `traceroute` help in network troubleshooting?

### ✨`traceroute` displays the path taken by packets from the local system to a remote host. It shows each intermediate router (hop) along the path and the time taken. It helps identify:
- Network delays
- Connection failures
- Routing issues

---

### ❓ Why is DNS used in networking?

### ✨DNS (Domain Name System) translates human-friendly domain names like `www.google.com` into machine-readable IP addresses like `142.250.182.14`. This is necessary because computers communicate using IP addresses, not domain names.

---

### ❓ How can you transfer a file securely in Linux?

### ✨Files can be transferred securely in Linux using the `scp` (Secure Copy) command, which uses SSH encryption.

Example:
```bash
scp file.txt user@192.168.1.10:/home/user/
```





