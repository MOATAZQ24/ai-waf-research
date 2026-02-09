# Digital Forensics & Incident Response (DFIR): Windows Attack Simulation

This repository contains a comprehensive set of resources, reports, and scripts focused on **Digital Forensics and Incident Response (DFIR)**. The project documents a simulated cyberattack on a Windows environment, detailing the methodology for evidence collection, artifact analysis, and reporting.

## 📌 Project Overview

The goal of this research is to provide a structured approach to forensic investigation following a security breach. It covers the end-to-end process from live evidence acquisition to post-mortem analysis of system artifacts.

### Key Focus Areas:
- **Live Evidence Collection:** Capturing volatile data such as running processes, network connections, and logged-on users.
- **Artifact Analysis:** Investigating Windows-specific artifacts like Prefetch files, Registry hives, and Event Logs.
- **Integrity Verification:** Using cryptographic hashing (SHA256) to ensure the chain of custody and evidence integrity.
- **Reporting:** Documenting findings in a clear, forensic-ready format.

---

## 📂 Repository Structure

| File | Description |
| :--- | :--- |
| `report.md` | **Main Forensic Report:** A detailed summary of the investigation, including methodology, findings, and recommendations. |
| `resource.md` | **Toolbox & References:** A curated list of tools (e.g., Volatility, FTK Imager, DumpIt) and commands used during the simulation. |
| `sheet.md` | **Cheat Sheet:** A quick reference for forensic commands and artifact locations. |
| `1.md` | **Technical Appendix:** Additional technical details and command-line examples. |

---

## 🛠️ Forensic Methodology

The investigation follows a rigorous forensic process:

1.  **Preparation:** Setting up a secure environment and administrative access for collection scripts.
2.  **Live Acquisition:** 
    - Processes: `tasklist`, `Get-Process`
    - Network: `netstat -ano`
    - Persistence: `schtasks`, `wmic startup`
3.  **Memory & Disk Imaging:** Creating forensic images of RAM and storage using industry-standard tools.
4.  **Artifact Extraction:** Collecting Event Logs (`.evtx`), Prefetch files (`.pf`), and Registry hives.
5.  **Analysis:** Building a timeline of events and identifying Indicators of Compromise (IoCs).

---

## 📊 Key Findings Summary

The simulation successfully identified several critical indicators:
- **Persistence Mechanisms:** Unauthorized scheduled tasks and startup items.
- **Malicious Execution:** Evidence of `POWERSHELL.EXE` and `CMD.EXE` usage found in Prefetch artifacts.
- **Network Anomalies:** Suspicious connections identified via `netstat` analysis.

---

## ⚖️ Disclaimer

This research is for educational and ethical security purposes only. All simulations were conducted in a controlled, isolated environment.

---

## 🎓 Author
**Moataz Qasem**  
Cybersecurity Professional | DFIR Researcher
