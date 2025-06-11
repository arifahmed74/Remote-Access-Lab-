# 🖥️ Remote Desktop Access Lab – Tier 1 Help Desk Simulation

This lab demonstrates how to set up a virtual environment using UTM on macOS and configure Remote Desktop Protocol (RDP) to remotely access a Windows 11/12 client machine. The setup simulates a real-world Tier 1 IT help desk scenario, including remote troubleshooting, network configuration, and firewall rule management.

---

## 🚀 Lab Objectives

- Set up a Windows 11/12 virtual machine using UTM on macOS
- Configure networking using **Bridged Mode** to simulate real network conditions
- Enable and secure **Remote Desktop Protocol (RDP)** access
- Connect to the virtual machine from the host macOS using the Microsoft Remote Desktop app
- Simulate Tier 1 support tasks via remote control

---

## 🧰 Tools & Technologies

- **UTM** (macOS virtualization tool)
- **Windows 11/12 ARM Insider ISO**
- **Microsoft Remote Desktop App (macOS)**
- **Windows Firewall Configuration**
- **Command Line Utilities** (`ipconfig`, `whoami`)
- **macOS Terminal** (for connectivity tests)

---

## 🛠️ Setup Overview

### 1. **Create Windows VM in UTM**
- Used the ARM64 Insider ISO to install Windows 11/12
- Allocated 4 GB RAM and 4 CPUs
- Enabled Bridged Networking through UTM VM settings

### 2. **Enable RDP on Windows**
- Turned on Remote Desktop via:
Settings > System > Remote Desktop > Enable
- Verified Windows Pro/Enterprise edition

### 3. **Configure Network Access**
- Switched UTM to **Bridged Mode** using macOS network interface (`en0` for Wi-Fi)
- Used `ipconfig` in Windows to get the bridged IPv4 address
- Confirmed network reachability using `ping` and `Remote Desktop`

### 4. **Allow Remote Access Through Firewall**
- Enabled Remote Desktop and ICMP (ping) in Windows Firewall
- Verified inbound rule: `Remote Desktop (TCP-In)` and `Echo Request - ICMPv4-In`

### 5. **Connect from Host Mac**
- Opened Microsoft Remote Desktop on macOS
- Added a new PC using VM’s bridged IP
- Authenticated using Windows local account
- Successfully connected and controlled the remote VM
  ---

## 📸 Screenshots
