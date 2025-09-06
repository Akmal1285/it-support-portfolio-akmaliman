# 🔄 Azure File Share – Backup & Recovery Lab

## 📌 Project Overview
Protected an existing **Azure File Share** by enabling backup in a **Recovery Services Vault**, triggered an on-demand backup, and restored a deleted file.  
This demonstrates cloud-based data protection and recovery skills.

---

## 🎯 Objectives
- Create a Recovery Services Vault
- Enable backup for an Azure File Share
- Run an on-demand backup
- Restore and verify a deleted file

---

## 🛠️ Tools & Skills Used
- **Azure Portal**
- **Recovery Services Vault**
- **Azure File Share**
- Skills: Backup & Recovery · Disaster Recovery · Cloud Administration

---

## 📸 Steps & Screenshots

### 1) Vault Created
Created a **Recovery Services Vault** in the same region as the storage account.  
![Vault overview](screenshots/vault_overview.png)

---

### 2) Backup Enabled for File Share
Configured the vault to protect the `labshare` Azure File Share.  
![Backup enabled](screenshots/backup_enabled.png)

---

### 3) On-Demand Backup Job
Triggered a manual backup to create a restore point.  
![Backup job](screenshots/backup_job.png)

---

### 4) Restore Job Result
Initiated a restore from the Recovery Services Vault. The backup job page confirms **Restore completed successfully**.  
![Restore result](screenshots/restore_result.png)

---

### 5) Verify Restored File
Confirmed the previously deleted test file reappears in the mapped `Z:` drive.  
![File restored](screenshots/file_restored.png)

---

## ✅ Results
- Recovery Services Vault deployed
- File share protected with scheduled and on-demand backups
- Verified point-in-time restore of deleted file

---

## 🚀 Key Takeaways
- Practical experience protecting **Azure Files** with cloud backup
- Learned backup policy basics and on-demand restore
- Enhanced portfolio with **disaster recovery** skills
