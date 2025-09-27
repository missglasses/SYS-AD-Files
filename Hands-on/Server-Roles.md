## Configure Server Roles (Windows Server 2016)

### Step 1: Open Server Manager
1. Launch **Server Manager**.
2. Go to **Add roles and features**.
3. Select **Role-based or feature-based installation** → **Next**.
4. Choose your server → **Next**.

### Step 2: Select Roles
- Check the following roles:
  - **Active Directory Domain Services (AD DS)**
  - **DHCP Server**
  - **DNS Server**
  - **File and Storage Services**
  - **Web Server (IIS)**
- Continue → Confirm selections.
- Check **Restart the destination server automatically if required**.
- Click **Install**.

### Step 3: Deployment Configuration
1. After installation, click the **flag with "!"** in Server Manager.
2. Select **Promote this server to a domain controller**.
3. Choose **Add a new forest**.
4. Enter your **Root domain name** (format: `<domainname>.com`, e.g., `domain-name.com`).
5. Enter a **Directory Services Restore Mode (DSRM) password**.
6. Go through **Additional Options** → **Paths** → **Review Options**.
7. Click **Install**.
   - The server will restart automatically.

### Step 4: Rename Computer 
1. Open **Advanced system settings** → **Computer Name** tab.
2. Click **Change** to set a descriptive name for your server (e.g., `CIN-server`). Also on client (e.g, `CIN-client`)
3. Restart the server if prompted.

### Step 5: Verify Promotion
- After restart, log in with your domain account (e.g., `domain-name\Administrator`).
- Confirm that the server is now a **Domain Controller**.
