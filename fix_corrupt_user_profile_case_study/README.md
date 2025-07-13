# 👤 Fixing a Corrupt User Profile – Case Study

## 📝 Issue Summary
User reports their Windows 10 account is not loading correctly. The system logs them into a temporary profile with missing files and settings. This is a common sign of a corrupt user profile.

---

## 🔍 Symptoms Observed
- Desktop is empty
- Temporary profile message appears
- User files not visible
- Changes do not save after reboot

---

## 🛠️ Troubleshooting Steps Taken

1. Rebooted into **Safe Mode** using `msconfig` or `Shift + Restart`.
2. Opened `lusrmgr.msc` to manage users.
3. Created a new **local administrator account** named `NewAdminUser`.
4. Rebooted normally and logged into the new user.
5. Verified everything loaded properly and the issue was resolved.
6. (Optional) Migrated files from:
7. Deleted or disabled the corrupt account.

---

## ✅ Result
- New user profile created successfully.
- User was able to log in and access system normally.
- System stopped logging into the temporary profile.
- Data was optionally transferred from the old profile.

---

## 🔧 Tools Used
- `lusrmgr.msc` (Local Users and Groups)
- `msconfig` (Safe boot)
- File Explorer
- Control Panel → User Accounts

---

## 📸 Screenshots
| Filename                          | Description                            |
|----------------------------------|----------------------------------------|
| `01_temp_profile_login.png`      | Temporary profile message              |
| `02_create_admin_account.png`    | New user creation in Local Users       |
| `03_user_account_created.png`    | Confirmation of new admin user         |
| `04_copy_files_from_old_user.png`| Migrating user data (optional)         |
| `05_successful_login_new_user.png`| New user login success                 |

---

## 🔐 Security Notes
- All actions performed locally in a VM
- No personal or sensitive data exposed
- Admin access was used responsibly

---

## 💡 What I Learned
- Identifying signs of a corrupt Windows profile
- Creating and managing local users with admin rights
- Navigating Safe Mode for recovery
- Migrating user data safely

---

> ✅ This is part of my local IT troubleshooting portfolio.  
> See also: [Slow PC Case Study](../Slow_PC_Troubleshooting_Case_Study)
