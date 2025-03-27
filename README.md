# PowerShell File Integrity Monitor (FIM) – CIA Triad Project

## Overview
This PowerShell-based **File Integrity Monitor (FIM)** project focuses on the **Integrity** pillar of the **CIA Triad**. The script allows users to create a **file hash baseline** and continuously **monitor for file changes** including **modifications, deletions, and creations**.

## Features
- Generate a secure **SHA-512 hash baseline** of all files in a directory
- Monitor files in real-time against the baseline
- Detect:
  - Modified files (hash mismatch)
  - New files (not in baseline)
  - Deleted files (missing from disk)
- Highlight status using **color-coded terminal output**
- Hashes and paths stored in a `baseline.txt` file using pipe-delimited format

## Learning Objectives
- Understand how file hashing ensures integrity
- Work with **PowerShell hashtables** and **Get-ChildItem**
- Build a PowerShell loop to simulate continuous file monitoring
- Develop secure scripting practices useful for **compliance (PCI-DSS, HIPAA)**

## Key Functions
- `Calculate-File-Hash` – Generates SHA-512 hashes
- `New-Baseline` – Scans and saves current file state
- `Start-Monitoring` – Continuously checks files against baseline

## Future Improvements
- Add recursive subdirectory scanning
- Implement user directory input
- Error handling and modular functions
- Real-time alerts via email/SMS

## Sample Output
```powershell
[+] New file detected: config.json
[!] File modified: settings.xml
[-] File deleted: credentials.txt
```

## Repository Structure
```
├── FileIntegrityMonitor.ps1       # Main PowerShell script
├── baseline.txt                   # Pipe-separated hash + path entries
├── README.md                      # Project documentation
```

## Conclusion
This lab provides hands-on experience with **file integrity monitoring** using **PowerShell**, ideal for security professionals and system administrators. It highlights **real-time detection of unauthorized changes**, supporting a foundational security control in your toolkit.

---
**Author:** Travis Johnson  
**Company:** 10Digit Solutions LLC  
**GitHub Repository:** [Add link when available]
