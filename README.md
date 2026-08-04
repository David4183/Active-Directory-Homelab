# Active-Directory-Homelab
##  Overview
This project was conducted to built a virtualized Windows Active Directory to develop hands-on experience with Windows Server administration, Active Directory Domain Services, DNS, networking, user management, and Windows client domain integration.

The lab simulates a small enterprise environment using VirtualBox and multiple Windows virtual machines.

## Lab Environment
Hypervisor: Oracle VirtualBox
Domain Controller Hostname	DC01
Client Hostname:	CLIENT01
Active Directory Domain	homelab.local
Domain Controller IP	192.168.1.10
Client IP	192.168.1.20
Network	VirtualBox Internal Network (homelab)

Lab Architecture
                     Active Directory Domain
                          homelab.local
                                |
                                |
                    Windows Server 2022
                         DC01
                    192.168.1.10
                                |
                  -------------------------
                  |                       |
                 AD DS                   DNS
                  |                       |
                  -------------------------
                                |
                         Internal Network
                            "homelab"
                                |
                                |
                    Windows 10 Client
                         CLIENT01
                    192.168.1.20
Objectives

The objectives of this lab were to:

Deploy a Windows Server 2022 virtual machine
Configure a static IP address on the Domain Controller
Install Active Directory Domain Services
Promote the server to a Domain Controller
Create the homelab.local Active Directory domain
Configure and utilize DNS for Active Directory
Deploy a Windows 10 client virtual machine
Configure static IP addressing on the client
Configure the client to use the Domain Controller for DNS
Test network connectivity between the client and Domain Controller
Test DNS resolution for the Active Directory domain
Join the Windows 10 client to the Active Directory domain
Authenticate to the domain using a domain user account
Implementation
1. Virtual Machine Deployment

Created two virtual machines in Oracle VirtualBox:

DC01

Operating System: Windows Server 2022
RAM: 4 GB
Storage: 60 GB
Network: Internal Network (homelab)

CLIENT01

Operating System: Windows 10
RAM: 4 GB
Storage: 50 GB
Network: Internal Network (homelab)

Both virtual machines were connected to the same VirtualBox Internal Network to allow communication between the Domain Controller and client.

2. Domain Controller Configuration

Installed Windows Server 2022 on DC01 and configured a static IP address.

The Domain Controller was assigned:

192.168.1.10

The Active Directory Domain Services (AD DS) role was installed through Windows Server Manager.

After installing AD DS, DC01 was promoted to a Domain Controller and the Active Directory domain was created:

homelab.local

3. Client Network Configuration

Windows 10 was installed on CLIENT01 and configured with a static IP address through the Windows graphical network settings interface.

The client was configured with the following network settings:

IP Address: 192.168.1.20
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.1.1
Preferred DNS Server: 192.168.1.10

The Domain Controller (DC01) was configured as the client's preferred DNS server to allow CLIENT01 to resolve the homelab.local Active Directory domain and locate domain services.

4. Connectivity Testing

Network connectivity between CLIENT01 and DC01 was tested using ping.

ping 192.168.1.10

DNS resolution was tested using nslookup.

nslookup homelab.local

Successful responses confirmed that CLIENT01 could communicate with the Domain Controller and resolve the Active Directory domain through the configured DNS server.

5. Joining the Client to the Domain

After verifying network connectivity and DNS resolution, CLIENT01 was joined to the homelab.local Active Directory domain.

Domain administrator credentials were provided during the domain join process.

CLIENT01 was then restarted to complete the domain join.

6. Domain Authentication

After restarting CLIENT01, the domain login option was selected from the Windows login screen.

A domain user account was used to authenticate to the Windows 10 client.

This verified that:

The client successfully joined the Active Directory domain
The client could communicate with the Domain Controller
DNS was correctly configured
Active Directory authentication was functioning
Testing and Verification

The following tests were performed:

Test	Purpose	Result
ping 192.168.1.10	Verify client-to-server connectivity	Successful
nslookup homelab.local	Verify DNS resolution	Successful
Domain Join	Verify Active Directory connectivity	Successful
Domain Login	Verify domain authentication	Successful
Skills Demonstrated
Windows Server 2022 Administration
Active Directory Domain Services (AD DS)
Domain Controller Deployment
DNS Configuration
Static IP Configuration
Windows 10 Client Configuration
Active Directory Domain Joining
Domain Authentication
Network Connectivity Testing
DNS Troubleshooting
Virtual Machine Deployment
Oracle VirtualBox
Future Improvements

Future enhancements to this lab may include:

Add a Windows 11 client to the Active Directory domain
Create Organizational Units (OUs)
Create and manage additional domain users
Create departmental security groups
Create separate OUs for IT, HR, and Finance
Configure Group Policy
Implement password complexity policies
Create shared folders
Configure NTFS and share permissions
Add a Windows Server member server
Expand the lab into a larger simulated enterprise environment
Project Outcome

Successfully deployed and tested a functional Active Directory environment consisting of a Windows Server 2022 Domain Controller and a Windows 10 domain client.

The lab demonstrates hands-on experience with deploying a Domain Controller, configuring Active Directory Domain Services, configuring DNS, assigning static IP addresses, testing network connectivity, joining a Windows client to an Active Directory domain, and authenticating users through the domain.

This project provides practical experience with foundational technologies commonly used in Windows-based enterprise IT environments and supports the development of skills relevant to entry-level IT support, help desk, and system administration roles.
