# Common Administrative Tasks

# PowerShell Commands Used

# Default Container Redirection
powershell
# View current default computers container
Get-ADDomain | Select ComputersContainer

# Redirect to custom OU
redircmp "OU=Workstations,OU=Computers,OU=Company,DC=homelab,DC=local"

# View current default users container  
Get-ADDomain | Select UsersContainer

# Redirect to custom OU
redirusr "OU=IT,OU=Users,OU=Company,DC=homelab,DC=local"
Verify Domain Health
powershell# Check domain controller diagnostics
dcdiag /v

# Verify FSMO roles
netdom query fsmo

# Check AD replication (when multiple DCs exist)
repadmin /replsummary
Next Administrative Tasks

- [] Create user naming standard (firstname.lastname)
- [] Implement password policy via GPO
- [] Create home folder structure
- [] Configure roaming profiles (optional)
