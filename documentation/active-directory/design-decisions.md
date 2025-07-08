# Active Directory Design Decisions

## OU Structure Philosophy

### Why Separate Company and Resources
- **Company OU**: Contains all user, computer, and group objects
- **Resources OU**: Contains service-specific objects (shares, printers)
- Separation allows different GPO inheritance paths

### OU vs Security Groups
- **OUs**: Used for Group Policy application and administrative delegation
- **Security Groups**: Used for resource permissions and access control
- GPOs can only be linked to OUs, not security groups

### Default Container Management
- Left default containers intact (required by AD)
- Implemented redirection for new objects
- Default containers cannot have GPOs applied

## Lessons Learned
1. Containers (folder icon) vs OUs (folder with book icon) are functionally different
2. Domain Controllers OU should never be moved or modified
3. Group organization is done through naming conventions, not nested OUs
4. Always specify OU when creating new objects to avoid default containers
