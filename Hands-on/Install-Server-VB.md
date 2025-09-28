# Windows 10 Client Setup (VirtualBox)

## 1. Install / Set Up Client VM
- **OS**: Windows 10 (22H2)
- **VirtualBox Settings**:
  - **Name**: (enter VM name)
  - **Motherboard (RAM)**: 2048 MB
  - **CPU**: 4 cores
  - **Storage**: Mount Windows 10 ISO
  - **Network**: Set to **Internal Network**

## 2. Configure Server VM (for Internal Network)
- Inside the **Server VM** (e.g., Windows Server 2016):
  - Go to **Network Adapter settings**
  - Assign a **static IP** (e.g., `192.....10.1`)
  - Subnet mask: `255.255.255.0`
  - Default gateway: `192.....10.1`
  - Preferred DNS: `192.....10.1`

## 3. Configure Client VM
- Inside the **Windows 10 client**:
  - Go to **Network Adapter settings**
  - Assign a **static IP** (e.g., `192.....10.2`)
  - Default gateway: `192.....10.1`
  - Preferred DNS: `192.....10.1`

## 4. Test Connectivity
- From the **client VM**, open **Command Prompt** and run:
  ```bash
  ping 192.....10.1
