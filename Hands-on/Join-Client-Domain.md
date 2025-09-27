# Client Join to Server Domain 

## 1. Rename Client Computer (Optional)
1. On the **Client VM**, go to:
   - **This PC → Properties → Advanced system settings → Computer Name → Change**
2. Set a descriptive name, e.g., `CIN-client`.
3. Restart if prompted.

---

## 2. Join Client to Domain
1. Go to **System Properties → Computer Name → Change → Member of: Domain**.
2. Enter the domain name: `domain-name.com`.
3. Enter **domain credentials** (e.g., `Administrator` from the server).
4. Restart the client to apply changes.

---

## 3. Configure DNS (Client & Server)
- **Server DNS**: `192.168.10.1`
- **Client DNS**: `192.168.10.1`  
  *(This ensures the client can resolve the domain and avoids “unknown domain” errors.)*

- Optional network configuration step:
  1. Go to **Network Adapter → IPv4 Properties**.
  2. Make sure **Preferred DNS Server = Server IP** (already done if above).

---

## 4. Test Connectivity
- On client, open **Command Prompt**:
```bash
ping CIN-server
nslookup CIN-server
