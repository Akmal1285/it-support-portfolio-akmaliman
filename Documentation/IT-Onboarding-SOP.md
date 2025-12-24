# Standard Operating Procedure (SOP): IT New Hire Onboarding

**Version:** 1.0  
**Owner:** IT Department / Akmal Iman  
**Last Updated:** December 2025  

---

## 1. Objective
To provide a standardized process for provisioning hardware, software, and identity access for new employees, ensuring compliance with **PDPA (Personal Data Protection Act)** and company security policies.

## 2. Phase 1: Identity & Access Management (IAM)
*Before the employee starts, the following must be configured:*

| Task | Platform | Description |
| :--- | :--- | :--- |
| **Email Creation** | M365 / Entra ID | Create `username@company.com`. |
| **License Assignment** | M365 Admin Center | Assign Business Premium / Standard license. |
| **Security Groups** | Active Directory | Add to department-specific groups (e.g., HR, Finance). |
| **MFA Setup** | Microsoft Authenticator | Enable "Require MFA" policy for the account. |

## 3. Phase 2: Hardware Provisioning
*All hardware must be recorded in the Asset Management log.*

1. **Asset Tagging:** Attach a physical asset tag (e.g., `MY-LAP-2025-001`) to the device.
2. **Imaging:** Ensure Windows 11 Pro is updated and "Company Portal" is installed.
3. **Security:** Verify **BitLocker Drive Encryption** is active and the Recovery Key is stored in Entra ID.

## 4. Phase 3: The "Day One" Handover
*Items to be completed during the physical handover:*

- [ ] **AUP Signing:** New hire signs the *Acceptable Use Policy* (IT Ethics).
- [ ] **MFA Enrollment:** Assist user in registering their mobile device for MFA.
- [ ] **Peripheral Handover:** Issue Mouse, Laptop Bag, and Privacy Filter.

---

## 5. References & Standards
* This SOP follows **ITIL v4** Service Transition best practices.
* Framework adapted from industry standard templates and customized for SME operations in Malaysia.
