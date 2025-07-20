# Privileged Access Model

## Account Tiers

### Tier 0 - Domain Admin Accounts
- **Naming Convention**: da.firstname.lastname
- **Usage**: Domain controller maintenance ONLY
- **Members**: da.john.smith (created, not used daily)
- **Restrictions**: 
  - NEVER used for email, web browsing, or daily tasks
  - NEVER used to log into workstations
  - Complex 20+ character passwords
  - MFA required (future implementation)

### Tier 1 - Server Admin Accounts  
- **Groups**: Server-Admins
- **Usage**: Member server administration
- **Rights**: Local admin on member servers (NOT domain controllers)

### Tier 2 - Workstation Support
- **Groups**: IT-Admins, Helpdesk-Staff
- **Usage**: Daily IT work, user support
- **Rights**:
  - Local admin on workstations (via GPO)
  - User/computer management in AD
  - No server access

## Delegation Model

### IT-Admins Can:
- Create/modify/delete user accounts
- Reset passwords and unlock accounts
- Join computers to domain
- Manage workstation GPOs
- Read LAPS passwords

### IT-Admins CANNOT:
- Modify Domain Admins group
- Access Domain Controllers
- Modify sensitive GPOs
- Change domain-wide settings

### Helpdesk-Staff Can:
- Reset passwords
- Unlock accounts
- Read user properties
- Basic troubleshooting

## LAPS Implementation (Planned)
- Local admin passwords randomized every 30 days
- IT-Admins can retrieve passwords when needed
- No shared local admin passwords

## Security Principles
1. **Least Privilege**: Users get minimum rights needed
2. **Separation of Duties**: Admin accounts separate from daily use
3. **Defense in Depth**: Multiple security layers
4. **Privileged Access Workstations**: (Future) Dedicated admin workstations
