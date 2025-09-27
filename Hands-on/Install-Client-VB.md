# VirtualBox Lab Setup (Server 2016 + Windows 10 Client)

---

## 1. Install / Set Up Server VM
- **OS**: Windows Server 2016 (Standard Evaluation)
- **VirtualBox Settings**:
  - **Name**: (enter VM name)
  - **Motherboard (RAM)**: 4096 MB
  - **CPU**: 4 cores
  - **Storage**: Mount Windows Server 2016 ISO
  - **Network**: Set to **Internal Network**

### Configure Server Network
- Inside **Windows Server 2016**:
  - Assign a **static IP**: `192.168.10.1`
  - Subnet mask: `255.255.255.0`
  - Default gateway: `192.168.10.1`
  - Preferred DNS: `192.168.10.1`

---

## 2. Install / Set Up Client VM
- **OS**: Windows 10 (22H2)
- **VirtualBox Settings**:
  - **Name**: (enter VM name, e.g., `Client22H2`)
  - **Motherboard (RAM)**: 2048 MB
  - **CPU**: 4 cores
  - **Storage**: Mount Windows 10 ISO
  - **Network**: Set to **Internal Network**

### Configure Client Network
- Inside **Windows 10 client**:
  - Assign a **static IP**: `192.168.10.2`
  - Subnet mask: `255.255.255.0`
  - Default gateway: `192.168.10.1`
  - Preferred DNS: `192.168.10.1`

---

## 3. Test Connectivity
- From the **client VM**, open **Command Prompt** and run:
  ```bash
  ping 192.168.10.1
