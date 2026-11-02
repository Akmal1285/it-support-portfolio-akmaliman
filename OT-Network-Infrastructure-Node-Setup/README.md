# Operational Technology (OT) Network Infrastructure Upgrade & Node Provisioning

## 📋 Project Overview
This case study details engineering support for an enterprise **Operational Technology (OT) Network Upgrade** in a high-availability transit environment. The project focused on transitioning critical communications infrastructure from standard MPLS to **MPLS-TP (Transport Profile)**, configuring industrial network hardware, conducting vendor technical research, performing fiber optic link diagnostics, and building technical SOPs.

---

## 📂 Project Deliverables & Reports
* 📄 **[OTDR Summary Report (PDF)](./docs/OTDR_Summary_Report.pdf):** Downloadable formal enterprise acceptance test report covering loss budget calculations and 48-core link validation.

---

## 🛠️ Key Technical Contributions

### 1. Protocol Architecture & Scope Analysis
* **MPLS-TP Protocol Transition:** Analyzed project specifications and scope of work for modernizing backbone communication links between central control nodes and transit stations to MPLS-TP.
* **Hardware & Switch Evaluation:** Studied technical datasheets and hardware architecture for new industrial Ethernet switches and network nodes required for high-reliability transmission.

### 2. XTRAN Node Configuration & SOP Creation
* **Initial Node Provisioning:** Successfully configured and established management connectivity with **XTRAN operational network nodes** using node management software during lab trials.
* **Standard Operating Procedure (SOP):** Authored a comprehensive, step-by-step SOP for initial XTRAN node setup, detailing software-to-hardware handshakes and baseline configurations to standardize future field deployments.

### 3. Fiber Optic Link Diagnostics & Acceptance Testing
* **OTDR & Power Meter Testing:** Executed testing across multi-core fiber links (up to 48 cores) to verify signal integrity, attenuation ($dB/km$), and splice/connector insertion loss ($dB$).
* **Loss Budget Verification:** Calculated maximum acceptable optical loss budgets for both 1310nm and 1550nm wavelengths to ensure total measured loss met enterprise acceptance criteria.
* **Documentation & Data Logging:** Formatted raw OTDR trace metrics into formal client-facing test summary reports and technical appendices.

### 4. Vendor Technical Research & Documentation
* **Product Datasheet Aggregation:** Conducted technical research (via supplier portals, direct email, and vendor inquiries) to collect, evaluate, and compile product specification sheets into formal technical reference documentation.
* **Integration Planning:** Participated in technical coordination syncs with project stakeholders, employers, and hardware suppliers to assess product integration into the live operational environment.

### 5. Cybersecurity & Data Resilience Evaluation
* **Endpoint Protection:** Researched enterprise endpoint protection architectures using **Trend Micro** tailored for specialized OT/industrial server and client environments.
* **Disaster Recovery & VM Backups:** Evaluated **Veeam Backup & Replication** solutions for automated virtual machine (VM) backups, disaster recovery strategies, and endpoint restoration.

### 6. Professional Development & Field Exposure
* Attended specialized manufacturer training on XTRAN node setup fundamentals.
* Completed introductory training on fiber optic splicing methodologies and cable handling.

---

## 📊 Appendix A: Fiber Optic Cable – OTDR Summary (Excerpt)

**Location:** Site-A to Site-B  
**Distance:** 4.20 km  
**Inspection Date:** 15 August 2026  

### Loss Budget Calculation
$$\text{Loss Budget} = [\text{length (km)} \times \text{attenuation/km}] + [\text{splice loss} \times \text{\# splices}] + [\text{connector loss} \times \text{\# connectors}]$$

* **1310nm Budget:** $[4.20\text{ km} \times 0.4\text{ dB}] + [0.2 \times 2] + [0.5 \times 2] = \mathbf{3.08\text{ dB}}$
* **1550nm Budget:** $[4.20\text{ km} \times 0.3\text{ dB}] + [0.2 \times 2] + [0.5 \times 2] = \mathbf{2.66\text{ dB}}$

*\text{Acceptable Loss Threshold: Total Measured Loss } < \text{ Loss Budget}*

| Core | Wavelength 1310nm - Distance (km) | Wavelength 1310nm - Total Loss (dB) | Wavelength 1310nm - Avg Loss (dB/km) | Wavelength 1550nm - Distance (km) | Wavelength 1550nm - Total Loss (dB) | Wavelength 1550nm - Avg Loss (dB/km) | Status |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Core 1** | 4.20 | 2.15 | 0.51 | 4.20 | 1.82 | 0.43 | **PASS** |
| **Core 2** | 4.20 | 2.20 | 0.52 | 4.20 | 1.85 | 0.44 | **PASS** |
| **Core 3** | 4.20 | 2.10 | 0.50 | 4.20 | 1.78 | 0.42 | **PASS** |
| **Core 4** | 4.20 | 2.25 | 0.53 | 4.20 | 1.88 | 0.45 | **PASS** |
| **Core 5** | 4.20 | 2.18 | 0.52 | 4.20 | 1.80 | 0.43 | **PASS** |
| **...** | ... | ... | ... | ... | ... | ... | **...** |
| **Core 48** | 4.20 | 2.22 | 0.53 | 4.20 | 1.84 | 0.44 | **PASS** |

---

## 🧰 Technical Skills & Tools Featured
* **Network Protocols:** MPLS, MPLS-TP, OT Communications, Industrial Ethernet.
* **Hardware & Equipment:** XTRAN Industrial Nodes, OTDR Meters, Optical Power Meters, Fiber Optic Cable Assembly.
* **Software & Security:** Trend Micro Endpoint Security, Veeam Backup & Replication, XTRAN Node Management Software.
* **Documentation & Operations:** Technical Writing, Loss Budget Calculations, SOP Development, Vendor Coordination, Technical Datasheet Analysis.
