### ⚙️ Windows 10 – PowerShell Local User Automation
Automated local user account creation using PowerShell scripting.

**Key Skills:** PowerShell · Automation · User Management

**Overview:**
This script automates the creation of multiple local user accounts on Windows 10. It prompts for passwords, assigns groups, and verifies the results — simulating how IT Support staff automate onboarding tasks.

**Commands Used:**
- `New-LocalUser`
- `Add-LocalGroupMember`
- `Get-LocalUser`

**Script:**
```powershell
# ================================
# PowerShell Local User Automation
# Author: Muhammad Akmal Iman
# ================================

# Define users to be created
$users = @(
    @{Name="support1"; FullName="Support Technician 1"; Description="IT Support Staff"},
    @{Name="intern1"; FullName="Intern Staff"; Description="Temporary Account"},
    @{Name="helpdesk1"; FullName="Helpdesk Analyst"; Description="Tier 1 Support"}
)

# Loop through each user and create the account if it doesn't exist
foreach ($user in $users) {
    if (-not (Get-LocalUser -Name $user.Name -ErrorAction SilentlyContinue)) {
        $password = Read-Host -Prompt "Enter password for $($user.Name)" -AsSecureString
        New-LocalUser -Name $user.Name -FullName $user.FullName -Description $user.Description -Password $password
        Add-LocalGroupMember -Group "Users" -Member $user.Name
        Write-Host "User $($user.Name) created successfully." -ForegroundColor Green
    }
    else {
        Write-Host "User $($user.Name) already exists. Skipping..." -ForegroundColor Yellow
    }
}

# Display all created users
Write-Host "`nAll Local Users:" -ForegroundColor Cyan
Get-LocalUser | Format-Table Name, Enabled, LastLogon
```

**Outcome:**
Efficient, repeatable user creation process for endpoint setup.


![Screenshot – PowerShell User Creation](screenshots/powershell_user_creation.png)

![Screenshot – Script](screenshots/script.png)

![Screenshot – Login Screen](screenshots/login_screen.png)







