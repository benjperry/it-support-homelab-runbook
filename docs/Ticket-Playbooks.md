# Ticket Playbooks

## 1) Password reset / account unlock
Symptoms: user can’t log in / locked / expired password  
Triage: confirm identity + username, check lockout status  
Steps: reset password, unlock account, force change at next logon (if needed)  
Verify: user logs in  
Notes: record what you did + timestamp

## 2) Access request (share/folder)
Symptoms: access denied to \\server\share  
Triage: confirm path + required level + approval  
Steps: add user to correct AD group; confirm share + NTFS permissions  
Verify: user can access required folder  
Notes: record group + justification

## 3) Device join / login issues
Symptoms: domain login fails / device not joined  
Triage: network, DNS, time sync  
Steps: join to domain, reboot, test domain login  
Verify: domain login works, correct OU  
Notes: record device name + OU

## 4) Drive mapping missing
Symptoms: mapped drive not appearing  
Triage: group membership, GPO scope, `gpresult`  
Steps: fix membership, `gpupdate /force`, relogin  
Verify: drive appears + access works  
Notes: record which GPO applied
