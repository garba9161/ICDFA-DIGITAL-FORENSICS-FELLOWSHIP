**Digital Forensics & Incident Response Portfolio**

**Institution:** International Cybersecurity and Digital Forensics Academy (ICDFA)

## Repository Overview

This repository holds my complete academic coursework, technical lab reports, evidence acquisition worksheets, code/command logs, and forensic analysis deliverables completed during Stage 2 (Digital Forensics & Incident Response Track) at ICDFA.

The curriculum spans six comprehensive modules covering basic computer and networking skills for forensic environments, core disk forensics using The Sleuth Kit (TSK) and Autopsy, evidence acquisition and chain-of-custody, mobile and IoT artifact extraction, AI-driven forensic analysis, and end-to-end case study investigations.

---

## Coursework & Deliverables

### Course 1: Basic Computer Skills for Digital Forensics (SBT-DF201)

Foundational computer literacy, terminal proficiency, file system navigation, and workspace preparation for forensic workstations.

📄 **Workspace Configuration & Forensic Environment Setup:** `[View Report]`

* **Overview:** Establishment of dedicated lab directory structures (`/evidence`, `/analysis`, `/recovered`, `/reports`), environment verification, initial tool dependency checks, and command-line file management.
* **Lab Deliverables:**
* `CIP_B101_Lab1a`: Number Systems, ASCII, Timestamps, and Data Representation. [View Report](<./Course-01-Basic-Computer-Skills/Reports/CIP_B101Lab 1a Ahmed Garba Assignment.pdf>)
* `CIP_B101_Lab1b`: PC Systems Fundamentals, Disk Sectors, and Partition Analysis (`diskpart`, `fdisk`, `parted`). [View Report](<./Course-01-Basic-Computer-Skills/Reports/CIP_B101Lab 1a Ahmed Garba Assignment.pdf>)
* `CIP_B101_Lab1c`: Windows Command Line for Digital Forensics (`systeminfo`, `icacls`, batch automation).[View Report](<./Course-01-Basic-Computer-Skills/Reports/CIP_B101Lab 1c Ahmed Garba Assignment.pdf>)
* `CIP_B101_Lab2a`: Linux Command Line for Digital Forensics (`stat`, `find`, `tree`, `grep`, network socket triage).[View Report](<./Course-01-Basic-Computer-Skills/Reports/CIP_B101Lab 2a Ahmed Garba Assignment.pdf>)
* `CIP_B101_Lab2b`: Advanced Linux Command Line for Digital Forensics (`dd`, standard streams `2>&1`, cross-platform `ncat` transfers). [View Report](<./Course-01-Basic-Computer-Skills/Reports/CIP_B101Lab 2b Ahmed Garba Assignment.pdf>)


---

### Course 2: Computer and Digital Forensics (SBT-DF202)

Core principles of digital investigations, evidence handling procedures, file system architecture, and forensic reconstruction using command-line and GUI utilities.

📄 **Digital Evidence Handling & Chain-of-Custody Framework (Lab 1):** `[View Report]`

* **Overview:** Establishment of forensic isolation procedures, write-blocker verification, mini chain-of-custody documentation, and baseline cryptographic hashing (`md5sum`: `a117773bcf1fc88ec0ab8e0a349fbbcb`, `sha256sum`: `3ce8053e4f3d9c8ab98b3aadb2480685efb8e4980d34297b83bd5a09b1a7b122`) for raw disk evidence (`Ch01InChap01.dd`).



📄 **Sleuth Kit (TSK) Command-Line Analysis & Artifact Recovery (Lab 1):** `[View Report]`

* **Overview:** File system layout analysis (`fsstat`), directory enumeration (`fls`), inode metadata examination (`istat`), deleted file recovery (`icat` for inode 15 `letter1.txt`), raw sector dumps (`blkcat` sector 312), and unallocated space analysis (`blkls`).



📄 **Autopsy GUI Case Analysis & Evidence Verification (Lab 1):**

* **Overview:** Graphical forensic case creation (`Lab1_Autopsy`), ingest module configuration, deleted file filtering, keyword search indexing for financial records (`INCOME.XLS`), artifact tagging, and automated report generation.


📄 **Multi-Vector Reconstruction & Cryptographic Hash Verification (Lab 1):**

* **Overview:** Parallel extraction of target evidence (`INCOME.XLS`) using `icat` inode extraction (inode 13), `blkcat` sector concatenation loops (sectors 285–311), and read-only loop mounting (`losetup`), verified via byte-for-byte MD5 (`6a2e65afc5af4fc5f9da2859df134eac`) hash comparison matrices.

  [View Lab 1 Report](<./Course-02-Computer-Digital-Forensics/Reports/Lab 1 SBT-DF202.pdf>)

📄 **Forensic USB Acquisition, Hash Verification & Evidence Validation (Lab 2):** [View Report](<./Course-02-Computer-Digital-Forensics/Reports/Lab 2 SBT-DF202 Garba.pdf>)

* **Overview:** Physical raw drive imaging of SanDisk Cruzer Blade (`\\.\PHYSICALDRIVE1`) using Exterro FTK Imager v8.3.0.27 to `.001` container format. Complete 100% hash match verification for MD5 (`7354741c934c2eb44fc25506130f21f0`) and SHA-1 (`db0fbb61b1ebe27277b9fe4ebf55d14d497cb143`) across all 7,864,320 physical sectors.



📄 **Data Carving, Hex Analysis & File Recovery (Lab 3):** [View Report](<./Course-02-Computer-Digital-Forensics/Reports/Lab 3 SBT-DF202 Garba.pdf>)

* **Overview:** Low-level binary pattern matching and raw data carving across corrupted file system metadata. Includes plain hex streaming (`xxd`) for header/footer signatures (`0xFFD8FFE1` / `0xFFD9`), OpenXML container extraction (`File_carving.docx`) via `binwalk` and `dd`, and rule-based automated carving from unallocated USB space (`usb_fat_carving.001`) via `scalpel` with `hashdeep` verification.

---

### Course 3: Basic Networking Skills for Digital Forensics (SBT-DF203)

*Module Status: Upcoming / In Progress*

📄 **Network Protocol Analysis & Packet Capture Assessment:** `[View Report]`

* **Overview (Global Standards & Course Expectations):** Capturing and analyzing live or offline network traffic using Wireshark and tcpdump. Focuses on protocol inspection (TCP/IP, UDP, DNS, HTTP/HTTPS), parsing pcap files for suspicious communication channels, identifying exfiltration vectors, and mapping network anomalies to the OSI and TCP/IP reference models.

---

### Course 4: Computer Forensics Case Study (SBT-DF204)

*Module Status: Upcoming / In Progress*

📄 **End-to-End Incident Investigation & Forensic Case Study:** `[View Report]`

* **Overview (Global Standards & Course Expectations):** Execution of a full, enterprise-level digital investigation scenario. Focuses on full-disk image triage, operating system artifact extraction (Windows Registry, Event Logs, LNK files, Prefetch, MFT/USN Journal), timeline construction, establishing root-cause compromise vectors, and authoring formal courtroom-admissible forensic reports.

---

### Course 5: Mobile and IoT Forensics Case Study (SBT-DF205)

*Module Status: Upcoming / In Progress*

📄 **Mobile & Smart Device Artifact Analysis:** `[View Report]`

* **Overview (Global Standards & Course Expectations):** Forensic extraction methodologies (Logical, File System, Physical) across Android/iOS devices and IoT/embedded systems. Focuses on parsing SQLite databases, messaging artifacts, location data/geolocation logs, application sandboxes, and correlating IoT sensor/telemetry logs with user events.

---

### Course 6: Artificial Intelligence for Forensics (SBT-DF206)

*Module Status: Upcoming / In Progress*

📄 **AI-Driven Data Parsing & Automated Pattern Recognition:** `[View Report]`

* **Overview (Global Standards & Course Expectations):** Integration of machine learning models and automated script pipelines to parse massive, unstructured forensic datasets. Focuses on automated log classification, intelligent Natural Language Processing (NLP) entity extraction across suspect communications, anomaly detection in user behaviors, and machine-assisted triage.

---

## Directory Structure

```text
.
├── Course-01-Basic-Computer-Skills/
│   └── Reports/
│       ├── CIP_B101_Lab1a_Data_Representation.pdf
│       ├── CIP_B101_Lab1b_PC_Systems_Partitioning.pdf
│       ├── CIP_B101_Lab1c_Windows_CLI.pdf
│       ├── CIP_B101_Lab2a_Linux_CLI.pdf
│       └── CIP_B101_Lab2b_Advanced_Linux.pdf
├── Course-02-Computer-Digital-Forensics/
│   └── Reports/
│       ├── Lab 1 SBT-DF202.pdf
│       ├── Lab 2 SBT-DF202 Garba.pdf
│       └── Lab 3 SBT-DF202 Garba.pdf
├── Course-03-Basic-Networking-Skills/
│   └── Reports/
├── Course-04-Computer-Forensics-Case-Study/
│   └── Reports/
├── Course-05-Mobile-IoT-Forensics/
│   └── Reports/
├── Course-06-AI-For-Forensics/
│   └── Reports/
└── README.md

```

---

## Licensing & Usage

These forensic deliverables were created as part of the International Cybersecurity and Digital Forensics Academy (ICDFA) Stage 2 Digital Forensics Programme and are shared strictly for educational and professional portfolio demonstration purposes.

---

## Contact

**LinkedIn:** Ahmed Garba

**GitHub:** `@garba9161`
