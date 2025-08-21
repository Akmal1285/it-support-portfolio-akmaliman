# 💾 Windows Backup & Restore Case Study

## 📘 Overview
This case study demonstrates how to configure Windows Backup, create a system backup, and restore deleted files using the built-in backup feature in Windows 10. It simulates a real-world IT support scenario where a user accidentally deletes important files and requests recovery.

---

## 🧠 Key Skills Demonstrated
- Configuring Windows Backup settings  
- Scheduling backups to an external drive or network location  
- Restoring files from backup  
- Understanding data protection best practices  

---

## 🛠️ Environment
- **Operating System:** Windows 10 Pro (VM)  
- **Storage:** Secondary virtual hard disk for backup target  
- **Network:** Not required  

---

## 🧪 Scenario
A user accidentally deletes important documents from their `Documents` folder. As the IT support technician, your task is to ensure backup was enabled, then recover the missing files from the last backup.

---

## 📝 Backup & Restore Checklist

1. **Open Backup Settings**  
   Go to **Control Panel > Backup and Restore (Windows 7)**.  

2. **Set Backup Destination**  
   Select a secondary virtual disk (e.g., E:) as the backup target.  

3. **Choose Backup Settings**  
   Let Windows choose recommended folders for backup.  

4. **Run Initial Backup**  
   Start the backup process and wait for completion.  

5. **Delete Test File**  
   Remove a file from `Documents` to simulate accidental deletion.  

6. **Open File History**  
   Select **Restore my files** in Backup and Restore.  

7. **Restore File**  
   Recover the deleted file to its original location.

---

## 📸 Screenshot Checklist
| Step | Screenshot Filename |
|------|----------------------|
| Backup settings screen | `01_backup_settings.png` |
| Destination selection | `02_select_destination.png` |
| Backup progress | `03_backup_in_progress.png` |
| Deleted file | `04_delete_file.png` |
| File History | `05_file_history_window.png` |
| Finished restore | `07_finished_restore.png` |
| Browse for file | `08_restored_file.png` |

> All screenshots are stored in the `screenshots/` folder for this project.

---

## ✅ Outcome
- Successfully configured Windows Backup  
- Verified backup by restoring a deleted file  
- Demonstrated ability to recover lost user data in a simulated incident  

---

## 💡 Key Learnings
- Importance of regular backups in IT environments  
- How to configure and manage Windows Backup  
- How to use restore functions to quickly resolve user issues
