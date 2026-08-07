# Active-Directory-Homelab
##  Overview
This project was conducted to built a virtualized Windows Active Directory to develop hands-on experience with Windows Server administration, Active Directory Domain Services, DNS, networking, user management, and Windows client domain integration.

The lab simulates a small enterprise environment using VirtualBox and multiple Windows virtual machines.

## Lab Environment
-  Virtualization Platform: Oracle VirtualBox
-  Domain Controller: Windows Server 2022 (DC01)
-  Client Machine: Windows 10 (CLIENT01)
-  Domain: homelab.local
-  Domain Controller IP: 192.168.1.10
-  Client IP: 192.168.1.20
-  Network: VirtualBox Internal Network (homelab)
-  Server Resources: 4 GB RAM, 60 GB storage
-  Client Resources: 4 GB RAM, 50 GB storage

## Technologies Used
### Active Directory Domain Services (AD DS)
-  Installed the Active Directory Domain Services role
-  Promoted Windows Server 2022 to a domain controller
-  Created the homelab.local domain
-  Configured and managed the Active Directory environment
-  Joined Windows 10 client to the domain
-  Verified domain authentication using a domain user account

### DNS Configuration
-  Configured DNS as part of the Active Directory environment
-  Configured the Windows 10 client to use the Domain Controller as its DNS server
- Tested DNS resolution using nslookup
-  Verified resolution of the homelab.local domain
### Network Configuration
-  Configured static IP addressing for the Domain Controller
-  Configured static IP addressing for the Windows 10 client
-  Connected both virtual machines to the same VirtualBox Internal Network
-  Tested connectivity between the client and Domain Controller using ping

