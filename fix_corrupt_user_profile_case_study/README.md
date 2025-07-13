# 👤 Fixing a Corrupt User Profile – Case Study

## 📝 Issue Summary
A local user named `TestUser` was logging into a temporary profile on Windows 10. The desktop was blank, and no files or personalization loaded. Any changes made were lost after logging out or restarting. This simulates a common user profile corruption issue.

---

## 🔍 Symptoms Observed
- Windows automatically loaded a **temporary profile**
- Desktop and Documents folders were empty
- Warning: _“You’ve been signed in with a temporary profile. Changes you make will not be saved.”_
- Original user data inaccessible in the session

---

## 🛠️ Troubleshooting Steps Taken

1. Logged in to `TestUser` and confirmed temporary profile behavior  
   📸 `01_tempt_profile_login.png`

2. Observed temporary profile warning on login  
   📸 `02_temp_profile_message.png`

3. Switched to the administrator account and created a new local user: `FixedUser`  
   📸 `03_create_admin_account.png`

4. Accessed `C:\Users\TestUser_backup` and transferred documents and files to  
   `C:\Users\FixedUser` after elevating permissions  
   📸 `04_copy_files_from_old_user.png`

5. Logged in to `FixedUser` and verified a stable and working profile  
   📸 `05_successful_login_new_user.png`

---

## ✅ Result
- The issue was resolved by setting up a new profile
- Key files from the old profile were preserved
- `FixedUser` is now used as the primary account without profile loading issues

---

## 🔧 Tools Used
- `lusrmgr.msc` (Local Users and Groups)
- File Explorer
- UAC permission elevation
- Windows 10 Virtual Machine

---

## 💡 What I Learned
- How to simulate and troubleshoot profile corruption
- How Windows handles temporary profiles
- How to securely transfer user data
- How standard user permissions affect profile recovery

---

## 🔐 Security Notes
- This was conducted entirely inside a **Windows 10 Virtual Machine**
- Dummy users and data used for testing purposes
- No internet or remote access tools involved

---

> 📁 Folder name: `fix_corrupt_user_profile_case_Study`  
> 🖼 Place screenshots in `/screenshots` subfolder  

