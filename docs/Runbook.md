# Runbook (AD DS + GPO + M365/Entra)

## Environment
- Windows Server (Domain Controller): AD DS + DNS
- Windows 11 client joined to domain
- Microsoft 365 tenant + Entra ID basics

## AD Users/Groups
- Users: create test users (e.g., test.user1)
- Groups: FileShare_Read, FileShare_Modify, VPN_Users (examples)
- Standard tasks:
  - Create user
  - Reset password / unlock account
  - Add/remove group membership

## GPO Basics (Lab)
- Password policy: minimum length + complexity (lab example)
- Drive mapping: map \\server\share to Z: for a specific group
- Verify GPO:
  - `gpupdate /force`
  - `gpresult /r`

## Troubleshooting checks (first-line)
- DNS: client should point to DC for DNS
- Time sync: large drift breaks logons
- Connectivity: can the client reach the DC (ping/name resolution)
- Event Viewer: check logon/policy/DNS errors
