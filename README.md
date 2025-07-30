# MemLabs Lab 4: Obsession - Shadows of the Deleted

## 📋 Challenge Overview

Lab 4 "Obsession" from MemLabs tests an analyst's willingness to go beyond default outputs and dig deep into memory artifacts. 
This challenge focuses on advanced process analysis, malware detection, and forensic interpretation of a Windows 7 SP1 memory dump.

## Objectives
- Identify and analyze malicious processes in memory
- Detect code injection and process hollowing techniques
- Uncover persistence mechanisms and evasion tactics
- Extract hidden artifacts and recover deleted data
- Demonstrate advanced memory forensics methodology

## 📊 Challenge Details

Challenge Name: Obsession: Shadows of the Deleted
Memory Dump: MemLabs-Lab4.7z
Target System: Windows 7 SP1 64-bit
Source: MemLabs Repository
Analysis Tool: Volatility 3 Framework 2.26.0
Environment: Kali Linux

## 🔍 Analysis Phases
### ✅ Phase 1: Process Mapping & Initial Reconnaissance
### Status: Complete | Duration: In Progress

### Key Findings Summary:

- Process Hollowing Detected: Multiple legitimate processes compromised
- Thread Injection: Abnormal thread counts in system processes
- Process Impersonation: Fake system processes with missing parameters
- Privilege Escalation: Suspicious user accounts with admin privileges

### Targeted Processes

- explorer.exe (Windows Shell)
- dllhost.exe (COM Surrogate)
- svchost.exe (Service Host)
- dwm.exe (Desktop Window Manager)
- taskhost.exe (Task Scheduler)

[📄READ Phase-1 Report [.md]](PHASE-1/PHASE1-Report.md)
[🔗READ Phase-1 Report [.PDF]](PHASE-1/PHASE1-Report.md)
[⤵️Download Phase-1 Report [.PDF]](https://github.com/jynxora/LAB-4-OBSESSION-Volatility-Scan/raw/main/PHASE-1/PHASE1-REPORT.pdf)


---

## 🔄 Phase 2: Deep Artifact Analysis
### Status: Coming Soon | ETA: 1-2 days

Network connection analysis
File system artifacts recovery
Registry key examination
Timeline reconstruction
Persistence mechanism identification

## 🏁 Phase 3: Flag Recovery & Advanced Techniques
### Status: Planned | ETA: 2-3 days

Deleted file recovery techniques
Memory carving and string analysis
Final flag extraction
Complete attack chain reconstruction
Defensive recommendations

---

### 🎯 Learning Outcomes
This analysis demonstrates:

Advanced process analysis techniques
Malware detection methodologies
Memory forensics best practices
Windows internals knowledge application
Systematic approach to complex investigations

### Feel free to:

Star ⭐ this repository for updates
Open issues for questions or discussions
Submit pull requests for improvements
Share your own analysis approaches

### ⚠️ Disclaimer
This analysis is conducted in a controlled environment for educational purposes. The memory dump contains simulated malware scenarios designed for learning digital forensics techniques.

### 📝 Citation
If you use this analysis in your research or learning:
Memory Forensics Analysis of MemLabs Lab 4: Obsession
Volatility 3 Framework Analysis - Phase 1: Process Mapping
[Jynx], July 2025

---

Next Update: Phase 2 analysis focusing on network artifacts and file system recovery techniques.

Stay tuned for the complete investigation journey!

Last Updated: July 30, 2025 | Analysis Status: Phase 1 Complete

🚀 Follow the Journey
🔗 Connect & Collaborate
