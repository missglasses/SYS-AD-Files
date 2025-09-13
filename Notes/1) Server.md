# 🖥️ Server 
## What is a Server?

- A **server** is a computer system that provides services to other computers (called **clients**).  
- **Clients** can connect through the **internet** or a **local area network (LAN)**.  


## Main Components of a Server
- Motherboard  
- CPU  
- Memory (RAM)  
- Hard Drive / Storage  
- Network Connection  
- Power Supply  

## Server Environment
- Installed in an **exclusive environment** like a server room.  
- Requires **air conditioning** to maintain temperature.  
- Placed on **server racks** that can stack multiple servers.  

## Redundancy & Reliability
- Servers should be **redundant** in case one fails.  
- Hardware redundancy includes:  
  - **Hot-swappable hard drives** in **RAID configuration**  
    - **RAID** (Redundant Array of Independent Disks): combines multiple drives for **fault tolerance** and/or **performance**.  
    - Example: RAID 1 mirrors data across two drives; RAID 5 uses striping + parity.  
  - **Redundant Fiber Channel Adapters** – ensures continuous network access.  
  - **Redundant Power Supplies** – prevents downtime in case one PSU fails.  
- To **avoid data loss** and maintain high availability.  

## How Server Works (Request–Response Model)
1. Client sends a **request** via the network.  
2. Server **receives** the request.  
3. Server **processes** the request and provides the information.  
4. Server ensures the client is **authenticated** before access.
   
```Browser → DNS(with IP) → Browser(URL & IP) → Web Server → Browser```

## Architectures
- **Client–Server Model** – clients request services, servers respond.  
- **Cloud Server Hosting** – multiple servers provide resources across distributed data centers.  
- Servers use **OS designed to handle thousands of connections** efficiently.  


## Real-Life Examples & Types of Servers

**Web Server**

  *Example:* - When a user types a URL in the browser:

   **Browser** asks the **DNS server** for the IP address.  
    - **Browser** sends an **HTTP request** to the web server using that IP.  
    - **Web server** processes it and sends back the webpage.  
    - **Browser** displays the content.

- **Database Server** – Stores and manages databases.  
  *Example:* A bank uses a database server to store customer account records.  

- **Application Server** – Runs applications for clients.  
  *Example:* A company runs an HR payroll system on an application server accessible by employees.  

- **Fax Server** – Handles fax transmissions.  
  *Example:* A law firm sends and receives digital faxes through a centralized fax server.  

- **File Server** – Stores and shares files.  
  *Example:* An office uses a file server so employees can share documents and project files.  

- **Mail Server** – Manages emails.  
  *Example:* Gmail or Outlook uses mail servers to send, receive, and store emails.  

- **Game Server** – Hosts multiplayer games.  
  *Example:* Fortnite or Minecraft uses dedicated servers to host online matches.  

- **Media Server** – Streams audio/video content.  
  *Example:* Netflix uses media servers to stream movies and shows to users worldwide.  

- **Print Server** – Manages printers in a network.  
  *Example:* A university uses a print server to control access to shared printers for students.  

- **VPS (Virtual Private Server)** – Virtualized server for isolated hosting.  
  *Example:* A small business rents a VPS to host its e-commerce website.  

- **Virtual Server** – Simulated server environment on physical hardware.  
  *Example:* An IT team runs multiple virtual servers on one physical machine to test different software.  

## ☁️ Cloud Providers
Major cloud platforms that offer server hosting and management:  
- **Azure (Microsoft)**  
- **AWS (Amazon Web Services)**  
- **GCP (Google Cloud Platform)**  

### Cloud Services
- **Sharing resources** among multiple clients.  
- **Data storage** for global access.  
- **Performing computations** for clients (e.g., AI, analytics, apps).  
- **Scalable infrastructure** – handle thousands of requests dynamically.  


## Server Operating Systems (OS)
Specialized OS designed for managing servers and heavy workloads:    
- Windows Server  
- Linux (Ubuntu Server, CentOS, Red Hat)  
- Unix-based systems  
