```
#
# Windows PowerShell script for AD DS Deployment
#

Import-Module ADDSDeployment
Install-ADDSForest `
-CreateDnsDelegation:$false `
-DatabasePath "C:\WINDOWS\NTDS" `
-DomainMode "Win2025" `
-DomainName "translogic21.test" `
-DomainNetbiosName "TRANSLOGIC21" `
-ForestMode "Win2025" `
-InstallDns:$true `
-LogPath "C:\WINDOWS\NTDS" `
-NoRebootOnCompletion:$false `
-SysvolPath "C:\WINDOWS\SYSVOL" `
-Force:$true
```

[Arxiu](https://drive.google.com/file/d/1fbbRB4azYnomreqkp8aWJkOULHEah7qf/view?usp=drive_link)
