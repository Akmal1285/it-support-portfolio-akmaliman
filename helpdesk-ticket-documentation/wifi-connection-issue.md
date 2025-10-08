# 📶 Windows 10 – Documenting Troubleshooting Steps (Simulated Wi-Fi Connectivity Case)

## 📌 Project Overview
This is a **simulated helpdesk case study** created to demonstrate structured troubleshooting and professional ticket documentation skills.  
The scenario focuses on diagnosing and resolving a **Wi-Fi connection issue** in Windows 10 Pro, one of the most common user-reported support problems.

---

## 🎯 Objectives
- Practice documenting troubleshooting steps clearly and logically.  
- Follow a structured workflow: identify → diagnose → resolve → verify.  
- Demonstrate communication and technical support skills through written documentation.  

---

## 🛠️ Tools & Skills Used
- Windows 10 Pro (Virtual Machine)  
- Network Troubleshooter  
- Command Prompt (`ipconfig`, `ping`, `netsh`)  
- Skills: Network Troubleshooting · Documentation · Communication  

---

## 📋 Simulated Ticket Documentation

### 🧩 Issue
**Simulated user “Sara”** reported that her laptop cannot connect to Wi-Fi.  
Other devices connect to the same network successfully, but her laptop shows *“No Internet, Secured.”*

---

### 🔍 Troubleshooting Steps

1. **Information Gathering**  
   - Verified Wi-Fi is enabled and connected to the correct SSID.  
   - Checked other devices — confirmed network is working.  

2. **Initial Diagnostics**  
   - Opened **Command Prompt** and ran:  
     ```cmd
     ipconfig /all
     ```  
     Found that the Wi-Fi adapter had an incorrect IP address (169.x.x.x).  

3. **Reset Network Stack**  
   - Ran the following commands:  
     ```cmd
     netsh winsock reset
     netsh int ip reset
     ```  
   - Restarted the laptop.  

4. **Manual IP Refresh**  
   - After restart, ran:  
     ```cmd
     ipconfig /release
     ipconfig /renew
     ```  
   - Verified a valid IP address was obtained from the router (192.168.x.x).  

5. **Connectivity Test**  
   - Ran `ping google.com` — successful replies confirmed internet access.  

---

### ✅ Outcome
Wi-Fi connectivity restored after resetting the TCP/IP stack and renewing IP configuration.  
Laptop successfully connected to the wireless network with stable internet access.

---

### 📌 Next Steps
- Advised user to monitor connection stability for 24 hours.  
- Suggested updating the Wi-Fi driver from manufacturer’s website.  
- Documented steps in the internal knowledge base for future reference.

---

### 🗒 Notes
- Scenario simulated for documentation and troubleshooting practice.  
- Demonstrates structured problem-solving and written communication skills.  
- Reflects a realistic first-line IT support task.  

---

## 📊 Key Takeaways
- Gained experience documenting network troubleshooting steps.  
- Practiced use of `ipconfig` and `netsh` for diagnosing Wi-Fi issues.  
- Reinforced importance of clear documentation in IT support environments.  

