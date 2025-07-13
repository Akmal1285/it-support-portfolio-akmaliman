## 🔐 Windows 10 Domain Join to Active Directory

📄 [Download Case Study](./Win10_Domain_Join_Case_Study.pdf)

This project demonstrates how a Windows 10 VM was configured to join an Active Directory domain hosted on a Windows Server 2019 domain controller.

### 🧠 Key Skills Demonstrated:
- Static IP and DNS configuration
- Domain join via GUI
- Authentication with domain user accounts
- Basic Active Directory networking

### 🧰 Environment:
- Domain Controller: Windows Server 2019 (`akmal.local`)
- Client: Windows 10 Pro
- VirtualBox Internal Network (`ADNet`)

### 📝 Domain Join Checklist (Windows 10 to Active Directory)

| Step # | Task                                                          | Notes / Results                            | Status |
|--------|---------------------------------------------------------------|--------------------------------------------|--------|
| 1      | Confirm network adapter settings (same internal network)      | Both VMs set to Internal Network `ADNet`   | ✅ Done |
| 2      | Set static IP on server                                       | 192.168.10.1, subnet 255.255.255.0         | ✅ Done |
| 3      | Set static IP on Windows 10 and point DNS to server           | 192.168.10.2, DNS = 192.168.10.1           | ✅ Done |
| 4      | Test connectivity with `ping`                                 | Replies received from server               | ✅ Done |
| 5      | Open System > Join domain                                     | Domain: `akmal.local`                      | ✅ Done |
| 6      | Authenticate using domain admin credentials                   | `Administrator / P@ssw0rd123`              | ✅ Done |
| 7      | Restart and log in as domain user                             | `akmal\testuser` login successful          | ✅ Done |
