# NETWORKWALKS-OUATTARA_CHEICK-B083-WK3-PASSWORD-CRACKING
# 🔐 Password Cracking & Cryptographic Auditing (Week 3)

Hands-on ethical hacking labs focused on PDF hash extraction, dictionary attacks, and password strength auditing using John the Ripper (JTR), Johnny GUI, and Networkwalks web tools.

## 🛠️ Project Overview
This repository documents the completion of the Week 3 mandatory practical modules in an authorized, isolated lab environment:
1. **W3-PM1:** Offline PDF password cracking using **John the Ripper (1.9.0-jumbo-1)** and **Johnny GUI** on Windows.
2. **W3-PM2:** Browser-based hash extraction and dictionary attack using **Networkwalks Hash Calculator** and **Password Cracker**.

---

## 📋 Module 1: Password Cracking with JTR & Johnny (`W3-PM1`)

### Execution Steps
1. **Environment Setup:** Downloaded and extracted John the Ripper (`64-bit Windows binaries`) and installed **Johnny GUI v2.2**, linking `john.exe` in Johnny's settings.
2. **Hash Extraction:** Extracted the cryptographic hash (`$pdf$4*4*128*...`) from `My Locked PDF1.pdf` and saved it into `hash1.txt`.
3. **Dictionary Attack:** Loaded `hash1.txt` into Johnny and executed the attack, recovering the plaintext password (`good-luck`).
4. **Verification:** Unlocked the target PDF file and captured the validation flag (`nw{cybersecurity_flag_captured_2608}`).

### 📸 Screenshots (`W3-PM1`)
* **Johnny Configuration (`john.exe` linked):**
<img width="977" height="692" alt="Detected John the Ripper 1 9 0-jumbo-1 OMP" src="https://github.com/user-attachments/assets/246ac869-8639-43f6-aa1f-5a4b57dabef7" />
* **Password Cracked (`good-luck`):**
  <img width="977" height="692" alt="crack" src="https://github.com/user-attachments/assets/912078ae-d023-4ef0-be81-39601121cbcd" />
* **Unlocked PDF & Flag Captured:**
  <img width="570" height="821" alt="congrat_first_hack" src="https://github.com/user-attachments/assets/e9491509-e5e2-4d7b-9899-5b54a740cdbb" />

---

## 📋 Module 2: Password Cracking with Networkwalks Tools (`W3-PM2`)

### Execution Steps
1. **Local Hash Extraction:** Uploaded `My-Locked-PDF1.pdf` into the **Networkwalks Hash Calculator** to parse the `$pdf$` hash locally in the browser.
2. **Dictionary Attack:** Pasted the extracted hash into the **Networkwalks Password Cracker** using the built-in 100-password wordlist, identifying the password (`password1`) at attempt 91/100.
3. **Verification:** Unlocked the PDF document and captured the validation flag (`nw{networkwalks_flag1_jtr_270521_1}`).

### 📸 Screenshots (`W3-PM2`)
* **Networkwalks Hash Calculator:**
  <img width="1920" height="1080" alt="extract_ahck" src="https://github.com/user-attachments/assets/def5ed4c-df9d-4eaa-8481-e7b7936e816b" />
* **Networkwalks Password Cracker (`password1`):**
  <img width="1920" height="1080" alt="trouvé" src="https://github.com/user-attachments/assets/90105576-8a35-4412-b030-0c9e0521f1f6" />
* **Unlocked PDF & Flag Captured:**
  <img width="1920" height="1080" alt="result_le_2" src="https://github.com/user-attachments/assets/c8971f8f-2951-4876-86a5-85756dfeccd7" />

---

## 🔍 Troubleshooting & Key Takeaways
* **Antivirus / Windows Defender Handling:** Ethical hacking binaries like John the Ripper trigger false-positive alerts in Windows Defender. Configured a temporary local lab exception to extract and run `john.exe` safely.
* **Hash Formatting Integrity:** Ensured the extracted hash in `hash1.txt` started strictly with `$pdf$` without trailing quotes or extra characters so JTR could auto-detect the PDF format.
* **Encryption vs. Hashing:** Reinforced the core distinction between two-way **Encryption** (protecting PDF confidentiality with a key) and one-way **Hashing** (verifying password digests via dictionary comparison).
