## Organizational Unit Structure

### Design Rationale
Created a hierarchical OU structure to support Group Policy application and administrative delegation. Structure mirrors typical business organization while keeping Resources separate for clarity.

### Implemented Structure
homelab.local/
├── Company
    ├── Users
    │   ├── IT
    │   ├── Sales
    │   ├── HR
    │   └── Finance
    ├── Computers
    │   ├── Workstations
    │   ├── Laptops
    │   └── Servers
    ├── Groups
    │   ├── Security
    │   └── Distribution
    └── Service Accounts
    |
    └── Resources
        ├── File Shares
        └── Printers

### Default Container Redirection
Configured default object placement to ensure new objects receive appropriate policies:
```powershell
# Redirect computers to join Workstations OU by default
redircmp "OU=Workstations,OU=Computers,OU=Company,DC=homelab,DC=local"

# Redirect users to IT OU by default  
redirusr "OU=IT,OU=Users,OU=Company,DC=homelab,DC=local"

** Security Groups**
Initial Security Groups Created
Created in Company\Groups\Security OU:
Group     Name        Purpose          Type        Scope
IT-Admins  Full administrative access  Security  Global
Helpdesk-Staff  Password resets, basic support  Security  Global
HR-UsersAccess to HR resourcesSecurityGlobal
Sales-UsersAccess to sales resourcesSecurityGlobal
Remote-Desktop-Users  RDP access to workstations  Security  Global
File-Share-Users  Basic file share access  Security  Global
Group Naming Convention

Department-based: [Department]-Users
Role-based: [Role]-Staff or [Role]-Admins
Resource-based: [Resource]-[Permission]
