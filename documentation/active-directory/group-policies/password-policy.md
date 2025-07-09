# Domain Password Policy Configuration

## Overview
Implemented NIST 800-63B compliant password policy emphasizing length and usability over complexity.

## GPO Details
- **Name:** Security - Domain Password Policy  
- **Linked to:** homelab.local (Domain root)
- **Created:** 07/09/25
- **Last Modified:** 07/09/25

## Password Policy Settings

### Configuration Summary
| Setting | Configured Value | Justification |
|---------|-----------------|---------------|
| Enforce password history | 10 passwords | Prevents password reuse while maintaining reasonable history |
| Maximum password age | 0 days (No expiration) | NIST guidance - passwords should only change when compromised |
| Minimum password age | 0 days | Allows immediate password changes when needed |
| Minimum password length | 14 characters | Exceeds NIST minimum for enhanced security |
| Password must meet complexity | Disabled | NIST guidance - length provides better security than complexity |
| Store passwords using reversible encryption | Disabled | Security best practice |

### Account Lockout Policy
| Setting | Value | Justification |
|---------|-------|---------------|
| Account lockout duration | 30 minutes | Balances security with user frustration |
| Account lockout threshold | 5 attempts | Prevents brute force attacks |
| Admin lockout | enable | prevents brute forcing of admin accounts - the most sensitive accounts there are.
| Reset lockout counter after | 30 minutes | Allows legitimate users to retry |

## Implementation Notes

### NIST 800-63B Alignment
This configuration follows current NIST Digital Identity Guidelines:
- **Length over complexity** - 14 character minimum provides strong security
- **No forced rotation** - Reduces predictable password patterns
- **No composition rules** - Allows natural, memorable passphrases
- **User-friendly approach** - Spaces and all characters permitted

### User Guidance
Users should be instructed to:
- Create passphrases using multiple words
- Example: "Coffee Tastes Better On Mondays!" (31 characters)
- Use spaces between words for readability
- Focus on length and memorability over complexity

### Future Enhancements
- [ ] Implement password blocklist checking
- [ ] Test password GP on various accounts
- [ ] Add breach password database integration  
- [ ] Create PowerShell script for common password detection
- [ ] Deploy user training on passphrase creation

## Testing to be Performed
- [] 1. Created test user account
- [] 2. Tested short password (13 chars) - properly rejected
- [] 3. Tested compliant passphrase - accepted
- [] 4. Verified no complexity requirements enforced
- [] 5. Confirmed account lockout after 5 failed attempts

## Deviations from NIST Minimums
- **Minimum length:** 14 characters (NIST minimum is 8)
  - Rationale: Enhanced security for administrative environment
  - Impact: Users must create longer but more memorable passphrases
