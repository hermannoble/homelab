================================
HOMELAB DOCUMENTATION
================================
Document Version: 1.0
Last Updated: [DATE]
Maintained By: [YOUR NAME]

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
- CPU: 
- RAM: [Amount] GB
- Storage: 1TB SSD [Brand/Model]
- NIC: [Onboard/Additional]
- GPU: [Model if applicable]

================================
OPERATING SYSTEM
================================
OS: Windows 11 Pro
Version: [Run winver to check]
Build: 
License Type: [Retail/OEM/Volume]
Install Date: 
Last Major Update: 

================================
NETWORK CONFIGURATION
================================
Primary NIC:
- IP Address: 192.168.1.50
- Subnet Mask: 255.255.255.0
- Gateway: 
- DNS Servers: 
- MAC Address: 

Remote Access:
- RDP Port: 3389 (default)
- Alternative Access: [VNC/Chrome Remote]

================================
VIRTUALIZATION PLATFORM
================================
Hypervisor: VirtualBox [Version]
Install Date: 
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
