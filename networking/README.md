## 🌐 Network Configuration & Troubleshooting (Windows 10 VM)

📄 [Download Case Study (PDF)](/networking/Network_Config_and_Troubleshooting_Case_Study.pdf)

---

### 🔧 What I Did
- 🖥️ Configured a static IP address on a Windows 10 virtual machine
- 📟 Verified configuration using `ipconfig /all`
- 🌐 Tested internet connectivity using `ping 8.8.8.8`
- 🚫 Simulated DNS failure by removing the DNS IP
- ✅ Restored DNS settings and confirmed internet access

---

### 🧠 Skills Demonstrated
- Network configuration and subnetting
- DNS troubleshooting
- Command-line networking tools (`ipconfig`, `ping`)
- Problem-solving in virtual environments

---

### 📝 Network Troubleshooting Checklist

| Step # | Task                                                                 | Observation / Notes                      | Status  | Success |
|--------|----------------------------------------------------------------------|------------------------------------------|---------|---------|
| 1      | Open Network Adapter Settings                                        |                                          | Done    | Y       |
| 2      | Configure static IP address (192.168.1.50)                           |                                          | Done    | Y       |
| 3      | Set subnet mask and default gateway                                 | Subnet: 255.255.255.0, Gateway: 192.168.1.1 | Done | Y       |
| 4      | Set preferred DNS to 8.8.8.8                                         |                                          | Done    | Y       |
| 5      | Verify IP settings using `ipconfig`                                 | IP: 192.168.1.50 confirmed               | Done    | Y       |
| 6      | Ping 8.8.8.8 to confirm internet access                              | Replies received                         | Done    | Y       |
| 7      | Remove DNS and ping `google.com` (simulate DNS failure)             | DNS resolution failed                    | Done    | Y       |
| 8      | Restore DNS settings                                                 | 8.8.8.8 re-entered                       | Done    | Y       |
| 9      | Ping `google.com` again to confirm DNS is working                   | Name resolved, ping successful           | Done    | Y       |
