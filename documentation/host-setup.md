================================
HOMELAB DOCUMENTATION
================================
Document Version: 1.0
Last Updated: [7/7/25]
Maintained By: [Herman Noble]

================================
PHYSICAL HOST DETAILS
================================
Hostname: LABHOST01
System Role: VM Host Server
Location: Under desk
Acquisition Date: 
Service Tag/Serial: 

HARDWARE SPECIFICATIONS:
- Model: Dell Optiplex [Model]
- CPU: i5-3470 @ 3.2 GHz
- RAM: 16 GB
- Storage: 1TB SSD Crucial
- NIC: [Onboard/Additional]
- GPU: [Model if applicable]

================================
OPERATING SYSTEM
================================
OS: Windows 10 Pro
Version: [Run winver to check]
Build: 
License Type: No License
Install Date: 
Last Major Update: 

================================
NETWORK CONFIGURATION
================================
Primary NIC:
- IP Address: 10.0.0.53
- Subnet Mask: 255.255.255.0
- Gateway: 10.0.0.1
- DNS Servers: 75.75.75.75 and 75.75.76.76
- MAC Address: 90:B1:1C:8B:3C:F7

Remote Access:
- RDP Port: 3389 (default)
- Alternative Access: [VNC/Chrome Remote]

================================
VIRTUALIZATION PLATFORM
================================
Hypervisor: VirtualBox 7.1.10
Install Date: 7/7/25
VM Storage Location: [Path]
Network Configurations:
- NAT Network: 
- Host-Only Network: 192.168.100.0/24

================================
VIRTUAL MACHINES
================================
VM #1: DC01
- Role: Domain Controller
- OS: Windows Server 2025
- vCPU: 2
- RAM: 4GB
- Storage: 60GB
- IP: 192.168.100.10
- Created: [Date]
- Last Snapshot: [Date]

[Additional VMs follow same format]

================================
SERVICES & ROLES
================================
Active Directory:
- Domain: homelab.local
- Forest Functional Level: 
- Domain Functional Level: 
- FSMO Roles: DC01

DHCP:
- Scope: 192.168.100.100-200
- Lease Duration: 
- Reservations: [List]

DNS:
- Primary: DC01 (192.168.100.10)
- Forwarders: 

================================
BACKUP & RECOVERY
================================
Backup Strategy: 
Backup Location: 
Backup Schedule: 
Last Successful Backup: 
Recovery Test Date: 

================================
MAINTENANCE LOG
================================
[Date] - Initial OS installation
[Date] - VirtualBox installed
[Date] - First VM created
[Date] - 

================================
KNOWN ISSUES / NOTES
================================
- 
- 
- 

================================
CREDENTIALS REFERENCE
================================
All passwords stored in KeePass database
Database Location: [Path]
Master Password Hint: [NEVER the actual password]

Standard Accounts:
- Local Admin: .\Administrator
- Domain Admin: HOMELAB\Administrator
- Service Accounts: [Listed in KeePass]

================================
NETWORK DIAGRAM
================================
[Link to diagram file or insert here]

Internet
   |
Router (192.168.1.1)
   |
   +-- Gaming PC (192.168.1.x)
   |
   +-- LABHOST01 (192.168.1.50)
         |
         +-- VirtualBox NAT
         |
         +-- Host-Only Network (192.168.100.0/24)
               |
               +-- DC01 (192.168.100.10)
               +-- [Future VMs]

================================
CHANGE LOG
================================
[Date] - [Your Name] - Initial documentation created
[Date] - [Your Name] - [What changed]****
