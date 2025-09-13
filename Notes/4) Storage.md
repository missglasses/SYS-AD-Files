# 💾 Storage Devices

Storage devices are just as important as servers since they are usually attached to them. There are multiple types, each with its advantages and trade-offs.

---

## HDD (Hard Disk Drive)
- **Oldest storage technology** (since the 1950s).  
- Uses **magnetic spinning disks** (mechanical).  
- Pros: **Cheap**, high **capacity**.  
- Cons: **Slow** compared to SSDs.  
- Still widely used for bulk storage.  

---

## SSD (Solid State Drive)
- Uses **flash memory** (no moving parts).  
- Pros: **Fast**, reliable, energy-efficient.  
- Cons: More expensive per GB.  
- Common setup:  
  - SSD → Operating System & Apps (fast boot, performance).  
  - HDD → Files & Data (cheap storage).  

📌 HDD + SSD together = **Locally Attached Storage (LAS)**  

---

## DAS (Direct Attached Storage)
- Storage **directly attached** to a server/computer (via SATA, USB, etc.).  
- Can be **internal** or **external** enclosures.  
- Pros: Low cost, simple, easy to deploy.  
- Cons: **Not scalable** (hard to expand as business grows).  
- Good for: **Small businesses** without large IT budgets.  

---

## NAS (Network Attached Storage)
- Storage device **connected to the network** (Ethernet).  
- Provides **file-level access** to multiple users/clients.  
- Built-in support for **RAID** at the hardware level.  
- Pros: Reliable, easy to scale (add/remove drives on the fly).  
- Cons: Can cause **network congestion** if many users access it.  
- Good for: **File sharing and backups** in small/medium businesses.  

---

## SAN (Storage Area Network)
- High-speed **dedicated storage network**.  
- Uses **Fibre Channel switches** instead of regular Ethernet.  
- Provides **block-level access** (appears as local disk).  
- Pros: **Very fast**, scalable, avoids Ethernet congestion.  
- Cons: **Expensive**, complex to manage.  
- Used in: **Enterprise-level environments** (banks, hospitals, data centers).  

---

## RAID (Redundant Array of Independent Disks)
- Combines multiple disks for **performance** and/or **fault tolerance**.  
- Example setups:  
  - RAID 1 → Mirroring (data copied across drives).  
  - RAID 5 → Striping + parity (balance of speed + redundancy).  
- NAS usually supports **hardware RAID**; DAS may use **software RAID**.  

---

## Software-Defined Storage (Microsoft Example)
- **Storage Spaces** (Windows feature):  
  - Combines multiple disks into a single **storage pool**.  
  - Allows carving out **virtual drives** (e.g., D:, E:).  
- **Storage Spaces Direct (S2D):**  
  - Enterprise/data center solution.  
  - Uses enclosures full of HDDs/SSDs to create massive storage clusters.  
  - Offers many RAID-like benefits at lower cost/complexity.  

---

## Key Takeaways
- **HDDs** = Cheap & high capacity, but slow.  
- **SSDs** = Fast & reliable, but expensive.  
- **DAS** = Simple, local, not scalable.  
- **NAS** = Network file storage, reliable, scalable, but shares network bandwidth.  
- **SAN** = High-performance dedicated storage network for enterprises.  
- **RAID** = Protects against data loss and improves performance.  
- **Software-defined storage** = Pools multiple drives for flexible, cost-effective storage.  

As a systems administrator, you’ll also:  
- Monitor storage capacity.  
- Plan for growth.  
- Prevent outages from "out of storage" issues.  

