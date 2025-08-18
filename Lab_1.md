#  **Experiment: Installing and Setting Up Linux on Windows**

## **Aim**
To learn how to download, install, and set up Linux on a Windows system using virtualization or WSL.

---

## **Reqiuremwnts**
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

---
