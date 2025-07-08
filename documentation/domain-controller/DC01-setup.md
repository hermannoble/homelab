# DC01 - Primary Domain Controller

## VM Specifications
- **VM Name:** DC01
- **Operating System:** Windows Server 2025 Standard (Desktop Experience)
- **vCPU:** 2
- **RAM:** 6GB
- **Storage:** 50GB (Dynamic VDI)
- **Network Adapters:** 
  - Adapter 1: NAT (Internet access)
  - Adapter 2: Host-Only (192.168.100.0/24)

## Initial Configuration
1. **Computer Name:** DC01
2. **IP Configuration:**
   - IP Address: 192.168.100.10
   - Subnet Mask: 255.255.255.0
   - Default Gateway: [blank]
   - Primary DNS: 127.0.0.1
   - Secondary DNS: 8.8.8.8

## Active Directory Installation
1. **Role Installation**
   - Installed via Server Manager
   - Role: Active Directory Domain Services
   - Installation Date: 7/7/25

2. **Domain Configuration**
   - Forest Root Domain: homelab.local
   - Forest Functional Level: Windows Server 2016
   - Domain Functional Level: Windows Server 2016
   - DSRM Password: [Stored in KeePass]

3. **FSMO Roles**
   - All roles hosted on DC01 (default for first DC)
   - Schema Master
   - Domain Naming Master
   - PDC Emulator
   - RID Master
   - Infrastructure Master

## Post-Promotion Tasks
- [ ] Configure DNS Forwarders
- [ ] Create OU Structure
- [ ] Configure Default Domain Policy
- [ ] Install DHCP Role
- [ ] Create initial user accounts
