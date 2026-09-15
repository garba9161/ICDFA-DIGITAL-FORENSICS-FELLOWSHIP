**Digital Forensics & Incident Response Portfolio**

**Institution:** International Cybersecurity and Digital Forensics Academy (ICDFA)

## Repository Overview

This repository holds my complete academic coursework, technical lab reports, evidence acquisition worksheets, code/command logs, and forensic analysis deliverables completed during Stage 2 (Digital Forensics & Incident Response Track) at ICDFA.

The curriculum spans six comprehensive modules covering basic computer and networking skills for forensic environments, core disk forensics using The Sleuth Kit (TSK) and Autopsy, evidence acquisition and chain-of-custody, mobile and IoT artifact extraction, AI-driven forensic analysis, and end-to-end case study investigations.

---

## Coursework & Deliverables

### Course 1: Basic Computer Skills for Digital Forensics (SBT-DF201)

Foundational computer literacy, terminal proficiency, file system navigation, and workspace preparation for forensic workstations.

📄 **Workspace Configuration & Forensic Environment Setup:**

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

📄 **Digital Evidence Handling & Chain-of-Custody Framework (Lab 1):** 

* **Overview:** Establishment of forensic isolation procedures, write-blocker verification, mini chain-of-custody documentation, and baseline cryptographic hashing (`md5sum`: `a117773bcf1fc88ec0ab8e0a349fbbcb`, `sha256sum`: `3ce8053e4f3d9c8ab98b3aadb2480685efb8e4980d34297b83bd5a09b1a7b122`) for raw disk evidence (`Ch01InChap01.dd`).



📄 **Sleuth Kit (TSK) Command-Line Analysis & Artifact Recovery (Lab 1):** 

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

📄 **Steganography Analysis, Payload Embedding & Password Cracking (Lab 4):** [View Report](<./Course-02-Computer-Digital-Forensics/Reports/Lab 4 SBT-DF202 Garba.pdf>)

* **Overview:** Hiding secret data inside image files (steganography) and recovering protected information. The lab involved inspecting a target cover image (`_tower_original_image_for_lab.bmp`), hiding a secret text file inside it using a password (`steghide embed`), and tracking how the image's digital fingerprint (MD5 hash) changed from `7f77e022...` to `95ca51e0...` after embedding. It also covered retrieving the hidden data (`steghide extract`) and using a password-cracking tool (`stegcracker`) with a wordlist (`rockyou.txt`) to automatically crack the protection and recover the passphrase (`1234`).

---


### **Course 03: Basic Networking Skills for Digital Forensics (SBT-DF203)**

📄 **HTTP Analysis Using Wireshark: Text Traffic (Lab 1):** [View Report](Course-03-Basic-Networking-Skills/Reports/Garba_Lab1_SBT-DF203.pdf)

**Overview:** Network traffic capture and packet encapsulation inspection of plaintext HTTP web sessions across local loopback (`lo`). Reconstructed TCP three-way handshake (`SYN` $\rightarrow$ `SYN-ACK` $\rightarrow$ `ACK`), extracted HTTP request headers (`GET /basic.html`, `User-Agent: curl/8.21.0`), evaluated server responses (`200 OK`, `Apache/2.4.68`), analyzed graceful connection closure (`FIN, ACK`), and verified packet file integrity using SHA-256 hashes (`c464a47532ee...`).

📄 **HTTP Analysis Using Wireshark: Embedded Image Traffic (Lab 2):** [View Report](Course-03-Basic-Networking-Skills/Reports/Garba_Lab2_SBT-DF203.pdf)

**Overview:** Identification, extraction, and forensic reconstruction of embedded multimedia files contained within unencrypted HTTP packet streams. Analyzed multi-object HTTP conversations, tracked TCP sequence/acknowledgement offsets during binary payload transmission, and extracted embedded media files directly from raw pcapng captures for hash verification and evidence recovery.

📄 **SYN Flood Pattern Investigation Using TShark (Lab 3):** [View Report](Course-03-Basic-Networking-Skills/Reports/Garba_Lab3_SBT-DF203.pdf)

**Overview:** Automated packet analysis and denial-of-service (DoS) forensic investigation using command-line TShark. Isolated TCP SYN flood attack patterns, evaluated half-open socket state metrics, analyzed source IP spoofing signatures, and filtered high-volume packet streams to construct incident timelines and impact assessments.

📄 **SMTP Email Traffic Forensics (Lab 4):** [View Report](Course-03-Basic-Networking-Skills/Reports/Garba_Lab4_SBT-DF203.pdf)

**Overview:** Deep packet inspection of Simple Mail Transfer Protocol (SMTP) traffic streams. Reconstructed email headers (`Received`, `From`, `To`, `Message-ID`), extracted MIME-encoded attachments, analyzed mail relay hops, and verified email sender authentication parameters from raw network communications.

📄 **ARP Poisoning Forensics (Lab 5):** [View Report](https://www.google.com/search?q=./Course-03-Basic-Networking-Skills/Reports/Lab%25205%2520SBT-DF203%2520Garba.pdf)

**Overview:** Forensic analysis of Address Resolution Protocol (ARP) spoofing and Man-in-the-Middle (MitM) network attacks. Identified gratuitous ARP packet floods, mapped IP-to-MAC mapping discrepancies, detected duplicate MAC address anomalies, and documented session interception timelines across local subnets.

📄 **Firewall Traffic Control and Forensic Verification (Lab 6):** [View Report](https://www.google.com/search?q=./Course-03-Basic-Networking-Skills/Reports/Lab%25206%2520SBT-DF203%2520Garba.pdf)

**Overview:** Inspection and verification of network packet filtering mechanisms and firewall log streams. Analyzed active connection tracking tables, evaluated dropped vs. accepted packet flags, verified stateful packet inspection rules, and correlated system firewall logs with raw network packet captures.

📄 **DNS Introduction and Traffic Analysis (Lab 7):** [View Report](https://www.google.com/search?q=./Course-03-Basic-Networking-Skills/Reports/Lab%25207%2520SBT-DF203%2520Garba.pdf)

**Overview:** Domain Name System (DNS) protocol traffic reconstruction and forensic analysis. Inspected UDP/TCP port 53 packet flows, analyzed A, AAAA, MX, and TXT record lookup requests, evaluated authoritative server responses, and constructed hostname resolution timelines.

📄 **DNS Spoofing Forensics (Lab 8):** [View Report](https://www.google.com/search?q=./Course-03-Basic-Networking-Skills/Reports/Lab%25208%2520SBT-DF203%2520Garba.pdf)

**Overview:** Forensic investigation of DNS cache poisoning and rogue DNS response injection attacks. Detected malicious IP redirection signatures, analyzed forged transaction IDs, evaluated TTL anomalies, and documented unauthorized domain redirection events.

📄 **WEP40 Wireless Packet Decryption and Aircrack Forensics (Lab 9):** [View Report](https://www.google.com/search?q=./Course-03-Basic-Networking-Skills/Reports/Lab%25209%2520SBT-DF203%2520Garba.pdf)

**Overview:** Here is the Markdown section formatted for **Course 03: Basic Networking Skills for Digital Forensics** to add directly into your `README.md`. Each entry matches your exact portfolio layout with relative file paths so the `View Report` links open your PDFs directly.

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
│       ├── Lab 3 SBT-DF202 Garba.pdf
│       └── Lab 4 SBT-DF202 Garba.pdf
├── Course-03-Basic-Networking-Skills/
│   └── Reports/
│       ├── Lab 1 SBT-DF203 Garba.pdf
│       ├── Lab 2 SBT-DF203 Garba.pdf
│       ├── Lab 3 SBT-DF203 Garba.pdf
│       ├── Lab 4 SBT-DF203 Garba.pdf
│       ├── Lab 5 SBT-DF203 Garba.pdf
│       ├── Lab 6 SBT-DF203 Garba.pdf
│       ├── Lab 7 SBT-DF203 Garba.pdf
│       ├── Lab 8 SBT-DF203 Garba.pdf
│       └── Lab 9 SBT-DF203 Garba.pdf
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
