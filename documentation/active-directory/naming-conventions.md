Active Directory Naming Convention Document
Here's a comprehensive naming standard for your homelab (and portfolio!):
markdown# Active Directory Naming Conventions
Document Version: 1.0
Last Updated: 07/09/25
Approved By: Herman Noble

## User Account Naming

### Standard Users
- **Format:** firstname.lastname
- **Example:** john.smith, jane.doe
- **Email:** firstname.lastname@homelab.local
- **Display Name:** Lastname, Firstname (Smith, John)

### Administrative Accounts  
- **Format:** adm.firstname.lastname
- **Example:** adm.john.smith
- **Purpose:** Separate privileged account for admins

### Service Accounts
- **Format:** svc.applicationname
- **Example:** svc.backup, svc.sql, svc.sharepoint
- **Description:** Always document purpose in description field

### Test Accounts
- **Format:** test.purpose
- **Example:** test.gpo, test.mail
- **Expiration:** Set expiration date when creating

## Computer Naming

### Domain Controllers
- **Format:** DC##
- **Examples:** DC01, DC02
- **Notes:** Sequential numbering, always two digits

### Servers
- **Format:** SRV-ROLE-##
- **Examples:** 
  - SRV-FILE-01 (File Server)
  - SRV-SQL-01 (SQL Server)
  - SRV-WEB-01 (Web Server)
  - SRV-APP-01 (Application Server)

### Workstations
- **Format:** WS-DEPT-###
- **Examples:**
  - WS-IT-001
  - WS-HR-001
  - WS-SALES-001

### Laptops
- **Format:** LT-DEPT-###
- **Examples:**
  - LT-IT-001
  - LT-SALES-002

### Virtual Machines (Testing)
- **Format:** CLIENT## (for generic test machines)
- **Example:** CLIENT01, CLIENT02

## Security Group Naming

### Department Groups
- **Format:** DEPT-Users or DEPT-Admins
- **Examples:** IT-Users, HR-Users, IT-Admins

### Resource Access Groups
- **Format:** Resource-Permission
- **Examples:** 
  - FileShare-HR-Read
  - FileShare-HR-Write
  - Printer-Color-Access

### Application Groups
- **Format:** App-ApplicationName-Role
- **Examples:** App-Salesforce-Users, App-Office365-Admins

### Role-Based Groups
- **Format:** Role-Description
- **Examples:** Helpdesk-Staff, Remote-Desktop-Users

## Organizational Unit Naming

### Standard OUs
- Use full words, not abbreviations
- Title case with spaces allowed
- Examples: "Human Resources" not "HR" for OU names

### OU Hierarchy
- Company > Department > Objects
- Resources > Type > Specific Resource

## Group Policy Object Naming

### Format: Policy Type - Target - Description
- **Examples:**
  - "Computer - All - Security Baseline"
  - "User - IT - Admin Tools"
  - "Computer - Servers - Windows Update Schedule"
  - "User - Sales - Desktop Restrictions"

## Other Conventions

### Sites (if using Sites and Services)
- **Format:** CITY-BUILDING
- **Example:** NYC-HQ, LA-BRANCH

### Printers
- **Format:** PRT-LOCATION-MODEL
- **Example:** PRT-IT-HP4000, PRT-LOBBY-CANON

### File Shares
- **Format:** Purpose or Department name
- **Examples:** HR-Documents, Public-Share, IT-Software

## General Rules

1. **No Special Characters** except hyphen (-) and underscore (_)
2. **No Spaces** in usernames or computer names
3. **Case Insensitive** but maintain consistency
4. **Maximum Length:**
   - Usernames: 20 characters (sAMAccountName limit)
   - Computer names: 15 characters (NetBIOS limit)
5. **Document Everything** - Use description fields

## Change Log
- 07/09/25 - Initial naming convention established
- [Future Date] - Added cloud resource naming
