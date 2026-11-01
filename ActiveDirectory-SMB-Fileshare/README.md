# Active Directory SMB File Share Implementation

## 📋 Project Overview
This lab project demonstrates the deployment and configuration of a centralized **SMB File Share** integrated within an **Active Directory (AD)** domain environment. The objective is to provision secure departmental file storage, configure share-level permissions, and manage access for specific domain user accounts using **Windows Server 2022** and **VMware**.

---

## 💻 Lab Architecture & Environment
* **Virtualization Platform:** VMware Workstation
* **Domain Controller & File Server:** Windows Server 2022 Standard Evaluation (`MDT-SRV-01`)
* **Domain Name:** `corp.ITLab.com`
* **Client Machine:** Windows client joined to the `corp.ITLab.com` domain

---

## 🛠️ Step-by-Step Implementation Guide

### 1. File Share Provisioning via Server Manager
* Navigated to **Server Manager** -> **File and Storage Services** -> **Shares**.
* Initiated the **New Share Wizard** using the **SMB Share - Quick** profile for fast and efficient deployment suited for Windows-based clients.
* Designated the local directory path (`C:\hr`) and assigned the network share name (`HR-Share`), establishing the remote path as `\\MDT-SRV-01\HR-Share`.

### 2. Configuring Share Permissions & Access Control
* Configured advanced sharing and permissions properties for the `HR-Share` folder.
* Integrated Active Directory security principals by browsing the domain directory (`corp.ITLab.com`).
* Assigned targeted permissions to specific domain users (e.g., `James Doe` / `Jdoe@corp.ITLab.com`) granting appropriate access levels (`Full Control`, `Change`, `Read`) to ensure controlled data access.

---

## 📸 Lab Screenshots & Configuration

| Action | Screenshot Reference | Description |
| :--- | :--- | :--- |
| **New Share Setup** | `servermanage addfileshare.png` | Accessing File and Storage Services shares in Server Manager. |
| **Share Profile** | `SetupFileShareQuick.png` | Selecting the **SMB Share - Quick** profile wizard. |
| **Path Configuration** | `setupfilesharepath.png` | Defining local path (`C:\hr`) and network share path (`\\MDT-SRV-01\HR-Share`). |
| **AD User Selection** | `Add user persmission.png` | Browsing and selecting domain users from `corp.ITLab.com` for permissions. |
| **Permission Tuning** | `permissionSetup.png` | Verifying and applying `Full Control`, `Change`, and `Read` permissions for targeted users. |

---

## 🔑 Key Takeaways & Skills Demonstrated
* **Windows Server Administration:** Managing Server Manager roles, file services, and storage provisioning.
* **Active Directory (AD DS):** Leveraging domain user objects and security principals for authorization.
* **SMB Networking & File Sharing:** Setting up network shares, paths, and share-level permissions.
* **Access Control Management:** Ensuring principle of least privilege by mapping individual/group permissions to shared enterprise resources.
