# 🖥️ Active Directory
- **Directory service** used in Microsoft environments.  
- Stores and organizes information about:
  - **Users** (names, phone numbers, passwords)  
  - **Devices** (computers, printers)  
  - **Applications**  
  - **Groups** (collections of users/resources with assigned rights)  
- Provides:
  - **Authentication** → verifies user identity.  
  - **Authorization** → grants access to permitted resources.  


## Core Functions
- **Centralized security management** → usernames & passwords stored in one location (Domain Controller).  
- **Single sign-on (SSO)** → one login grants access to multiple resources.  
- **Group-based management** → permissions and policies applied via groups.  
- **Reduces redundancy** → reset a password once instead of on every computer.  


## AD Objects
- **Users** → people with accounts.  
- **Resources** → hardware/software like printers, file shares, computers.  
- **Groups** → collections of users/resources for easier management.  

Objects are organized into:  
- **Domains** → autonomous management units.  
- **Organizational Units (OUs)** → subdivisions inside domains (e.g., departments, locations).  

## Group Policy Objects (GPOs)
- Collection of policy settings applied to OUs/domains.  
- Examples:
  - Restrict folder/resource access.  
  - Disable specific executables.  
  - Apply company-wide security policies.  

## AD Hierarchy
- **AD Tree** → a domain and its subdomains (child domains).  
- **AD Forest** → collection of multiple trees.  
- **Trust Relationships** → allow users from one domain to access resources in another.  
  - Types: intra-forest, inter-forest, inter-subdomain.  

**Example:**  
- Forest = company.  
- Trees = subsidiaries (e.g., USA, France).  
- Domains = cities (e.g., New York, Chicago).  
- OUs = departments (e.g., Marketing, HR).  
- Objects = users/resources inside those OUs.  

## AD Architecture
- **Domain Controllers (DCs)** → servers running AD DS (Active Directory Domain Services).  
  - Handle user logins, authentication, and directory queries.  
  - Synchronize data across the forest for consistency.  
- **Read-Only Domain Controllers (RODCs)** →  
  - Store a read-only copy of AD.  
  - Used in remote/branch sites for faster access and security.  

## Why Active Directory Matters
- Simplifies **administration**.  
- Provides **centralized authentication & authorization**.  
- Improves **security** with fine-grained access control.  
- Scales to manage **thousands of users and devices**.  

