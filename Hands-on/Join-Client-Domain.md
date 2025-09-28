# Windows Domain Join & DNS Configuration Guide

## Step 1: Join Client to Domain
(Client PC)

  Right-click **This PC** → Click **Properties** → Click **Advanced system settings**
  Go to the **Computer Name** tab

### 2. Change Domain Membership
- Click the **Change** button
- In the dialog:
  - Select **Domain**
  - Enter the domain name:  
    `domain-name.com`
- Click **OK**

### 3. Authenticate
- When prompted, enter domain administrator credentials:


- Click **OK**

### 4. Restart Client
- Restart the computer when prompted

**If the domain shows as "Unknown" after the restart** , check the steps below

---

##   Step 2: Network Configuration (Already Done)

Ensure the following **IPv4 settings** are applied on the client machine:

| Setting               | Value              |
|----------------------|--------------------|
| Preferred DNS Server | `192.....10.1`     |

---

## Troubleshooting "Domain Unknown" Error
 ### Open DNS Manager (on Server)

1. On the domain controller, go to:
2. In **DNS Manager**:
- Expand your server name
- Right-click **Reverse Lookup Zones** → Click **New Zone**

3. In the New Zone Wizard:
- Click **Next**
- Choose **Primary Zone**
- Select:
  ```
  To all DNS servers running on domain controllers in this domain (Windows 2000 compatibility)
  ```
- Click **Next**
- Choose **IPv4 Reverse Lookup Zone** → Click **Next**
- Enter **Network ID**:
  ```
  192......10
  ```
  This creates the zone:
  ```
  10......192.in-addr.arpa
  ```
- Click **Next**
- Select: **Allow only secure dynamic updates**
- Click **Finish**

---

### Step 2: Register DNS Records on Server

Open **Command Prompt as Administrator** on the **Server**, and run:

```
cmd
:: Register the server’s DNS records
ipconfig /registerdns

:: Clear DNS cache
ipconfig /flushdns

:: Register client's DNS record with the DNS server
ipconfig /registerdns

:: Forward lookup (short name)
nslookup CIN-server

:: Forward lookup (FQDN)
nslookup CIN-server.cincin.com

:: Reverse lookup (IP to name)
nslookup 192.....10.1

## Step 5: Create PTR Record 

If `nslookup 192.....10.1` fails to resolve:

1. On the **Server**, open **DNS Manager**.
2. Navigate to:
3. Right-click the zone → Click **New Pointer (PTR)**.
4. Fill in:
- **Host IP address:** `1` (last octet of `192.....10.1`)
- **Host name:** `CIN-server.cincin.com`
5. Click **OK**.

Return to the client and re-run:

```cmd
nslookup 192.....10.1


```
It should show:
Name: CIN-server.cincin.com
Address: 192.....10.1
