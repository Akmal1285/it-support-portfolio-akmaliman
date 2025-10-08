# 🖨 Windows 10 – Documenting Troubleshooting Steps (Simulated Printer Issue)

## 📌 Project Overview
This is a **simulated helpdesk case study** created to demonstrate professional documentation of a printer troubleshooting workflow.  
Printer-related problems are among the most common helpdesk requests.  
This case focuses on diagnosing and resolving a **printer not printing** issue in Windows 10 Pro.

---

## 🎯 Objectives
- Practice documenting structured troubleshooting steps for printer issues.  
- Apply logical diagnostics to identify service and driver-related causes.  
- Demonstrate written communication and resolution documentation skills.

---

## 🛠️ Tools & Skills Used
- Windows 10 Pro (Virtual Machine)  
- Services Console (`services.msc`)  
- Devices and Printers  
- Command Prompt (`net start spooler`)  
- Skills: Hardware Troubleshooting · Documentation · Communication  

---

## 📋 Simulated Ticket Documentation

### 🧩 Issue
**Simulated user “Farid”** reported that his printer is installed and visible in “Devices and Printers,” but print jobs stay stuck in the queue and nothing is printed.  

---

### 🔍 Troubleshooting Steps

1. **Information Gathering**  
   - Confirmed printer is powered on and connected via USB/Wi-Fi.  
   - Verified the correct printer is set as default in *Devices and Printers*.  

2. **Checked Print Queue**  
   - Opened *Control Panel → Devices and Printers → Printer Queue*.  
   - Found multiple documents in “Pending” state.  

3. **Restarted Print Spooler Service**  
   - Opened **Services Console (services.msc)**.  
   - Located **Print Spooler** → Stopped → Started service again.  
   - Alternatively, used CMD:  
     ```cmd
     net stop spooler
     net start spooler
     ```

4. **Cleared Print Queue Files**  
   - Stopped Spooler service again.  
   - Deleted temporary print files from:  
     ```
     C:\Windows\System32\spool\PRINTERS
     ```  
   - Restarted Print Spooler.  

5. **Reinstalled Printer Driver**  
   - Removed printer device → Reinstalled using *Add Printer Wizard*.  
   - Verified correct driver installed.  

6. **Tested Printing**  
   - Printed test page → Successfully completed.

---

### ✅ Outcome
Printer successfully resumed printing after restarting the **Print Spooler service**, clearing the print queue, and reinstalling the printer driver.  
System confirmed “Test Page Printed Successfully.”

---

### 📌 Next Steps
- Advised user to monitor printer behavior for recurring issues.  
- Recommended updating printer drivers regularly.  
- Logged resolution steps for knowledge base reference.

---

### 🗒 Notes
- Scenario simulated for documentation and troubleshooting practice.  
- Reflects real-world helpdesk workflow for hardware and service issues.  
- Focus on clarity and logical sequencing of steps.

---

## 📊 Key Takeaways
- Practiced diagnosing and resolving printer spooler issues.  
- Demonstrated structured documentation for hardware troubleshooting.  
- Strengthened communication and technical writing skills.
