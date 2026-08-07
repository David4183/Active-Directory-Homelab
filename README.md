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

## Lab Setup Process
### Step 1: Domain Controller Setup
-  Created a Windows Server 2022 VM named DC01
-  Allocated 4 GB RAM and 60 GB storage
-  Connected the VM to the homelab Internal Network
-  Installed Windows Server 2022
-  Configured a static IP address of 192.168.1.10
-  Installed the Active Directory Domain Services role through Server Manager
-  Promoted DC01 to a Domain Controller
-  Created the homelab.local Active Directory domain
### Step 2: Client Configuration
-  Created a Windows 10 VM named CLIENT01
-  Allocated 4 GB RAM and 50 GB storage
-  Connected the VM to the same homelab Internal Network
-  Installed Windows 10
-  Configured a static IP address of 192.168.1.20
-  Configured the Domain Controller (192.168.1.10) as the client's DNS server
### Step 3: Connectivity & DNS Testing
-  Tested connectivity from CLIENT01 to DC01 using ping
-  Tested DNS resolution using nslookup
-  Verified that CLIENT01 could resolve homelab.local
-  Confirmed communication between the client and Domain Controller
### Step 4: Domain Join & Authentication
-  Joined CLIENT01 to the homelab.local domain
-  Provided domain administrator credentials during the domain join process
-  Restarted the client to complete the domain join
-  Logged into the client using a domain user account
-  Verified successful Active Directory authentication

## Skills Demonstrated
-  Windows Server 2022 administration
-  Active Directory Domain Services (AD DS)
-  Domain Controller deployment
-  DNS configuration and management
-  Static IP configuration
-  Windows 10 client configuration
-  Active Directory domain joining
-  Domain authentication
-  Network connectivity testing
-  DNS troubleshooting
-  Virtualization (Oracle VirtualBox)
-  Basic TCP/IP networking

## Key Learnings
-  Understanding of Active Directory domain environments
-  Hands-on experience deploying a Windows Server Domain Controller
-  Understanding of the relationship between Active Directory and DNS
-  Experience configuring static IP addresses and DNS settings
-  Experience joining Windows clients to an Active Directory domain
-  Understanding of domain-based authentication
-  Experience troubleshooting basic network and DNS connectivity

## Future Improvements
-  Add a Windows 11 client
-  Create Organizational Units (OUs)
-  Create additional domain users and security groups
-  Configure Group Policy Objects (GPOs)
-  Implement password complexity policies
-  Create shared folders
-  Configure NTFS and share permissions
-  Add a Windows Server member server
-  Expand the environment into a larger simulated enterprise network

## Resources & References
-  Active Directory home lab setup guide used as a reference for the initial lab configuration
-  Microsoft documentation for Windows Server and Active Directory Domain Services
