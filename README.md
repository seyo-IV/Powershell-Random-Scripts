
# Get-Effective-Permissions-EXCEL
  To use Get-Effective-Permissions-EXCEL u need to alter Local_Group_Prefix(If you are using local and global groups from Mictosoft best practice) to suit your company standards. The module Active Direcotry and NTFSSecurity is also required.
  
  New in v2 is that the script can detect nested AD-Groups and take them to show the REAL permissions.

# GUI
  I do recomend to start the scripts with a shortcut with the following content in Target: [%windir%\System32\WindowsPowerShell\v1.0\powershell.exe - windowstyle hidden -Noninteractive -ExecutionPolicy Bypass –Noprofile -file "\\SERVER\PATH\TO\SCRIPT"]
  
  Or you use the shortcut.ps1 to create the shortcut to the GUI with above parameters. Note that the script shortcut.ps1 should be in the same directory where the GUI script is. You can then palce the shortcut wherever you like.
  
  
  Membershipt.ps1 shows groupmembership of a user, group and the member of a group.
  wildcard_search.ps1 does a wildcard AD-Query for user or group.
  permission.ps1 shows the NTFS-Permissions to a specific path.
  
  For the GUIs you will need the Active Directory Module for wildcard_search.ps1 and membership.ps1.
  For GUI permissions.ps1 you wil need the NTFSSecurity Module.
  
  When using the "Search User" button in some GUIs you should define additional collums, like Username etc.

# Awesome PowerShell Profile
Obivously you would need an AD-Module for ufind and gfind.

The profile has some iteresting buildin functions and I think every admin should have them in his belt. To use the Profile rename Awesome_Microsoft.PowerShell_profile.ps1 to Microsoft.PowerShell_profile.ps1 and place it under [%userprofile%\documents\WindowsPowerShell\].

  ufind = Find AD-User based on Name and other criterias.
  
  gfind = Find AD-Group based on SamAccountName.
  
  sfind = Find string in files in a directory.
  
  sinfo = Get server info.
  
  perm = Get NTFS Permissions on a UNC path.
  
  pwgen = Generate a password.
 
  # Tip #
Open the desired script, then choose raw and follow the steps.

To download only one script and not the whole repo use [wget -O somefile.ps1 -uri https://raw.githubusercontent.com/seyo-IV/Powershell/master/Get-ADGroup-Member-CSV.ps1]
