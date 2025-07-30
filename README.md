# MemLabs Lab 4: Obsession - Shadows of the Deleted

📋 Challenge Overview
Lab 4 "Obsession" from MemLabs tests an analyst's willingness to go beyond default outputs and dig deep into memory artifacts. This challenge focuses on advanced process analysis, malware detection, and forensic interpretation of a Windows 7 SP1 memory dump.
🎯 Objectives

Identify and analyze malicious processes in memory
Detect code injection and process hollowing techniques
Uncover persistence mechanisms and evasion tactics
Extract hidden artifacts and recover deleted data
Demonstrate advanced memory forensics methodology

📊 Challenge Details

Challenge Name: Obsession: Shadows of the Deleted
Memory Dump: MemLabs-Lab4.7z
Target System: Windows 7 SP1 64-bit
Source: MemLabs Repository
Analysis Tool: Volatility 3 Framework 2.26.0
Environment: Kali Linux

🔍 Analysis Phases
✅ Phase 1: Process Mapping & Initial Reconnaissance
Status: Complete | Duration: In Progress
Key Findings Summary:

Process Hollowing Detected: Multiple legitimate processes compromised
Thread Injection: Abnormal thread counts in system processes
Process Impersonation: Fake system processes with missing parameters
Privilege Escalation: Suspicious user accounts with admin privileges

Critical Discoveries:

Malicious svchost.exe (PID 864) - 900+ threads (normal: 10-150)
Duplicate dwm.exe processes with abnormally low handle counts
Code Injection in explorer.exe, dllhost.exe with identical shellcode
Fake taskhost.exe processes missing legitimate GUID parameters
Suspicious user accounts: "eminem" and "SlimShady" with admin rights

🔄 Phase 2: Deep Artifact Analysis
Status: Coming Soon | ETA: 2-3 days

Network connection analysis
File system artifacts recovery
Registry key examination
Timeline reconstruction
Persistence mechanism identification

🏁 Phase 3: Flag Recovery & Advanced Techniques
Status: Planned | ETA: 4-5 days

Deleted file recovery techniques
Memory carving and string analysis
Final flag extraction
Complete attack chain reconstruction
Defensive recommendations

🛠️ Tools & Environment
ToolVersionPurposeVolatility3.2.26.0Primary memory analysis frameworkKali LinuxLatestAnalysis environmentstringsGNU binutilsString extractiongrepGNU grepPattern matching
📈 Technical Highlights
Process Analysis Methodology
bash# Core process enumeration
vol -f MemoryDump_Lab4.raw windows.pslist

# Malware detection
vol -f MemoryDump_Lab4.raw windows.malfind  

# Command line analysis
vol -f MemoryDump_Lab4.raw windows.cmdline

# DLL analysis  
vol -f MemoryDump_Lab4.raw windows.dlllist

# Security identifier analysis
vol -f MemoryDump_Lab4.raw windows.getsids
Key Malware Indicators Identified
🚨 Code Injection Signature
assemblymov r10d, 0x80/0x81/0x82    ; System call numbers
movabs rax, 0x7fefe93a138    ; Malicious handler address  
jmp qword ptr [rax]          ; Jump to injected code
nop                          ; Padding
🔍 Process Anomalies

Thread Count: svchost.exe with 900+ threads (typical: 10-150)
Handle Count: dwm.exe with 1-2 handles (typical: 200-800)
Command Line: taskhost.exe missing GUID parameters
Multiple Instances: Duplicate explorer.exe and dwm.exe processes

📊 Attack Vector Analysis
Identified Techniques

T1055: Process Injection
T1055.012: Process Hollowing
T1134: Access Token Manipulation
T1136: Account Creation
T1543: Persistence via Services

Targeted Processes

explorer.exe (Windows Shell)
dllhost.exe (COM Surrogate)
svchost.exe (Service Host)
dwm.exe (Desktop Window Manager)
taskhost.exe (Task Scheduler)

🎯 Learning Outcomes
This analysis demonstrates:

Advanced process analysis techniques
Malware detection methodologies
Memory forensics best practices
Windows internals knowledge application
Systematic approach to complex investigations

📚 Documentation Structure
├── Phase1_ProcessMapping/
│   ├── pslist_analysis.md
│   ├── malfind_results.md
│   ├── cmdline_investigation.md
│   └── privilege_analysis.md
├── Phase2_DeepAnalysis/ (Coming Soon)
├── Phase3_FlagRecovery/ (Coming Soon)
└── tools_and_techniques.md
🚀 Follow the Journey
📱 Social Media Updates

Twitter/X: Real-time analysis updates and insights
LinkedIn: Professional analysis summaries
Medium: Detailed technical blog posts

🔗 Connect & Collaborate
Feel free to:

Star ⭐ this repository for updates
Open issues for questions or discussions
Submit pull requests for improvements
Share your own analysis approaches

⚠️ Disclaimer
This analysis is conducted in a controlled environment for educational purposes. The memory dump contains simulated malware scenarios designed for learning digital forensics techniques.
📝 Citation
If you use this analysis in your research or learning:
Memory Forensics Analysis of MemLabs Lab 4: Obsession
Volatility 3 Framework Analysis - Phase 1: Process Mapping
[Your Name/Handle], July 2025

Next Update: Phase 2 analysis focusing on network artifacts and file system recovery techniques.
Stay tuned for the complete investigation journey! 🔍

Last Updated: July 30, 2025 | Analysis Status: Phase 1 Complete
