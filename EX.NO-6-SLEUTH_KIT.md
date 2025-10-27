# 🕵️‍♂️ **Experiment No. 06 — Digital Forensic Analysis using Sleuth Kit (TSK)**

## 🔍 **Overview**

The **Sleuth Kit (TSK)** 🧰 is a versatile suite of command-line tools used in **digital forensics**.  
It enables investigators to analyze disk images 🖥️, uncover deleted files 🗑️, and extract critical digital evidence 🔎 from storage devices.  
This document walks through the complete process of using Sleuth Kit on a **Windows** system to perform forensic analysis.

---

## ⚙️ **Step 1: Installing Sleuth Kit**

1. **Download the Tool:**  
   - Head over to the official Sleuth Kit page or use this link:  
     👉 [Download Sleuth Kit](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v)  
   - Choose the latest stable **Windows-compatible** version.

2. **Installation Process:**  
   - Run the installer and follow the setup wizard 🪄.  
   - Once done, TSK will be ready to use on your system!

---

## 💾 **Step 2: Acquire the Disk Image**

Before analysis, a **forensic disk image** (a perfect bit-by-bit copy) of the device is needed.

1. **Create Disk Image:**  
   - Use tools like **FTK Imager** 🧮 or **`dd`** to create an exact copy.  
   - Save it in a TSK-supported format: `.dd`, `.raw`, `.img`, or `.E01`.

2. **Sample Evidence Files:**  
   - For this lab, download the following from the provided link:  
     📁 `4Dell Latitude CPi.E01`  
     📁 `4Dell Latitude CPi.E02`

---

## 💽 **Step 3: Mounting the Disk Image (Optional)**

Mounting lets you access the disk image as if it were a normal drive.

- Use **OSFMount** 🧷 to mount the image in **read-only mode**.  
- 🔒 *Note: This is optional but helps when browsing the file system.*

---

## 🧭 **Step 4: File System Analysis with TSK**

Now let’s dive into Sleuth Kit tools 🧠 to inspect the file system.

### 🧑‍💻 Navigate to the TSK Directory

```bash
cd "C:\Program Files (x86)\sleuthkit-4.14.0-win32\bin"
```
<img width="1152" height="648" alt="image" src="https://github.com/user-attachments/assets/ded4f754-30df-4614-8cd2-1e0075318f38" />

---

### 🔍 Identify File System Type

<img width="670" height="28" alt="image" src="https://github.com/user-attachments/assets/4f70ce98-f568-4675-a07d-8bce9cd1aac2" />

<img width="1481" height="736" alt="image" src="https://github.com/user-attachments/assets/bc9239f3-5026-4e4e-b02c-edf6883d996f" />
💡 *Displays key details about the file system type and structure.*

---

### 🧩 View Partition Layout

<img width="758" height="43" alt="{83ADE046-B594-4BD0-B0D1-7D839AAE7905}" src="https://github.com/user-attachments/assets/56d6b105-4b1f-4b25-a2b0-fc98d6eaeef7" />

<img width="1481" height="736" alt="image" src="https://github.com/user-attachments/assets/fb1a6c58-85ed-4a9b-b69f-59b42ac320a9" />
➡️ *Lists all partitions and their respective start/end addresses.*

---

### 📂 List Files and Directories

<img width="800" height="44" alt="{D918A9A5-822D-47FF-9F81-6E780DDA5BF9}" src="https://github.com/user-attachments/assets/67450bf9-03d6-4de7-9805-be9954bdc9df" />

<img width="1434" height="752" alt="image" src="https://github.com/user-attachments/assets/aeef93d3-836c-4669-8382-8225f400184a" />
🔸 *Recursively lists files and folders with their inode details.*

---

### 🗃️ Recover Deleted Files

<img width="912" height="51" alt="{34E95F97-E8EC-4641-AF25-5DD80EBA6BE4}" src="https://github.com/user-attachments/assets/e36467f2-f108-4135-886a-693393cf8044" /><img width="572" height="32" alt="{F358B18F-8CE0-46EC-9735-367FC74ED38D}" src="https://github.com/user-attachments/assets/c2a75b6f-669e-418e-a682-f45909095c50" />

<img width="1907" height="298" alt="{07F2406F-6EEE-4BBC-BD95-A85584865323}" src="https://github.com/user-attachments/assets/442c2a95-c324-4c42-8a58-0c2fa6655631" />


💾 *Recovers a deleted or existing file by its inode number.*

---

## 🕰️ **Step 5: Metadata Analysis**

To uncover file history and access details, view the file’s metadata.
<img width="901" height="40" alt="{8BB42C2E-6AC0-4ED6-A165-89D11F0BE7EF}" src="https://github.com/user-attachments/assets/02e0e0ef-12a7-413d-b4a9-ba5f4de0575f" /><img width="584" height="36" alt="{E7C73E8B-9084-489D-8D32-BF10AD812055}" src="https://github.com/user-attachments/assets/35974be6-b314-4b54-98b6-bbb89b269993" />


🧠  
![WhatsApp Image 2025-10-26 at 22 58 58_65998012](https://github.com/user-attachments/assets/48b51664-732c-44ae-98d5-1c27a22069e3)

📘 *Displays file attributes such as MAC times (Modified, Accessed, Changed), size, and allocation info.*

---


## 📜 **Step 6: Report Generation**

After completing your analysis:

1. **Compile All Outputs:**  
   Collect files like `filesystem_info.txt`, `partitions.txt`, `file_list.txt`, and `timeline.txt`.

2. **Interpret and Document:**  
   Write a clear summary 📑 explaining your findings, methods used, and any key recovered evidence.

---

## 🔐 **Step 7: Evidence Preservation**

Ensuring the integrity of evidence is the final and most important step 🧳.

1. **Archive Evidence Securely:**  
   Use encryption 🔒 and hashing 🧮 to store your disk image and findings.

2. **Maintain Chain of Custody:**  
   Keep the evidence in a secure location following proper forensic protocols ⚖️.

---

## ✅ **Conclusion**

Using the **Sleuth Kit (TSK)**, investigators can efficiently extract, analyze, and preserve digital evidence 💾.  
It remains one of the most reliable and open-source forensic toolkits for digital investigation 🚔.
