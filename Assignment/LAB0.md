#  **Experiment: Installing and Setting Up Linux on Windows**

## **Aim**
To learn how to download, install, and set up Linux on a Windows system using virtualization or WSL.

---

## **Reqiurements**
- Windows 10/11 PC
- Internet connection
- VirtualBox / VMware (for virtualization) OR Windows Subsystem for Linux (WSL)

---

## **Procedure**

### **Step 1: Download Linux ISO**
1. Open your browser and visit the [Ubuntu official website](https://ubuntu.com/download/desktop).
2. Choose the latest LTS (Long Term Support) version.
3. Click **Download**.

**Image for above step**  
![install Ubuntu ISO](<ubuntu download 2025-08-18 163707.png>)

---

### **Step 2: Install VirtualBox** (if using Virtual Machine)
1. Go to [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads).
2. Download the Windows installer.
3. Run the installer and complete the setup.

**Image for above step** 

![install virtual box](<virtual box download 2025-08-18 164121.png>)

---

### **Step 3: Create a New Virtual Machine**
1. Open VirtualBox.
2. Click **New**.
3. Enter a name (e.g., *Ubuntu*), select **Linux** and **Ubuntu (64-bit)**.
4. Allocate memory (recommended: 4GB+).
5. Create a virtual hard disk (recommended: 25GB+).

**Image for above step** 

![Create Virtual Machine](<setup  2025-08-18 165234.png>)

---

### Step 4: Mount the Linux ISO
1. Select your new VM and click **Settings**.
2. Go to **Storage**.
3. Under "Controller: IDE", click the empty disk icon.
4. Choose the Ubuntu ISO you downloaded earlier.

**Image for above step**  

![Memory allocation](<memory1  2025-08-18 165510.png>)
![Memory allocation](<memory2 2025-08-18 165853.png>)

---
### Step 6: Complete Installation
1. Wait for installation to finish.
2. Restart the VM when prompted.
3. Login with your username and password.

**Image for above step**  

![Ubuntu Desktop](<Installed 2025-08-18 170307.png>)

# 🎉**congrats you just installed linux**🎉



# 📌Extra Questions:
### ❓ What are two advantages of installing Ubuntu in VirtualBox?

 Ans- Two main advantages of installing Ubuntu in VirtualBox are:

Safe Testing Environment 🛡️
You can try out Ubuntu without affecting your main operating system (like Windows).
If something goes wrong (e.g., system crash, virus, misconfiguration), only the virtual machine is affected, not your actual computer.

Flexibility and Convenience ⚡
You can run Ubuntu alongside your existing OS without needing dual boot.
VirtualBox allows easy snapshots (save system state) and quick resets, making it simple to experiment, learn, or test software.


### ❓ What are two advantages of dual booting instead of using a VM?

Ans- Two main advantages of dual booting Ubuntu instead of using a virtual machine (VM) are:

Better Performance ⚡
Since Ubuntu runs directly on the hardware (not through a virtualization layer), it can use the full CPU, GPU, and RAM without sharing resources with another OS.
This is especially useful for heavy tasks like gaming, video editing, or software development that requires high performance.

Full Hardware Access 💻
Dual boot gives Ubuntu direct access to all system hardware (Wi-Fi adapters, graphics cards, USB devices, etc.), which might not work properly or be limited inside a VM.
This makes it more reliable for testing drivers, running resource-heavy applications, or using specialized hardware.

 

---