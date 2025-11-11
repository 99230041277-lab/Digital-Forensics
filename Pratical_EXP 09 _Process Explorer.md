### 🎯 **Aim**

To analyze and identify suspicious or malicious processes running in a Windows operating system using **Process Explorer**, a Sysinternals forensic tool. This experiment aims to understand process behavior, verify authenticity, and evaluate system activity for potential threats. 🔍

---

### 🔄 **Forensic Investigation Flow (30 Marks)**

1. **Evidence Preparation:** Obtain and isolate the target system suspected of malicious activity. 🖥️
2. **Tool Acquisition:** Download **Process Explorer** from Microsoft Sysinternals to maintain forensic integrity. 🌐
3. **Tool Initialization:** Run `procexp.exe` or `procexp64.exe` as **Administrator** to view active processes. 🛡️
4. **Process Tree Analysis:** Observe processes in a tree structure to identify parent–child relations. 🌳
5. **Color-Coded Observation:** Recognize process states using Process Explorer’s color indicators (Green – New, Red – Terminated, Pink – Suspended). 🎨
6. **Suspicious Process Identification:** Find unknown or high-resource processes from non-system directories. ⚠️
7. **Digital Signature Verification:** Use **Properties → Image** tab to verify process authenticity. 🧾
8. **Path and Description Check:** Legitimate files are in `C:\Windows\System32`; others may be suspicious. 📁
9. **Resource Usage Monitoring:** Track abnormal CPU, memory, or disk usage. 💻
10. **Network Activity Analysis:** Inspect **TCP/IP** tab for unknown external connections. 🌐
11. **Documentation:** Record process details (PID, path, signature status) for evidence. 📝
12. **Threat Verification:** Cross-check with **VirusTotal** or **ProcessLibrary** databases. 🦠
13. **Containment:** Kill or suspend malicious processes. ❌
14. **File Removal:** Delete confirmed malicious executables. 🧹
15. **System Validation:** Run a full system antivirus scan. ✅

---

### ⚙️ **Tool Application and Analysis Accuracy**

| **Aspect**            | **Explanation**                                                                           |
| :-------------------- | :---------------------------------------------------------------------------------------- |
| **Tool Used**         | Process Explorer (Sysinternals Suite by Microsoft)                                        |
| **Purpose**           | To identify and analyze suspicious running processes                                      |
| **Accuracy Method**   | Checked via **Digital Signatures**, **File Path**, **Resource Use**, **Network Analysis** |
| **Observation Focus** | Unsigned executables, unusual paths, excessive CPU usage                                  |
| **Result Validation** | Verified with **VirusTotal** and company details                                          |
| **Accuracy Level**    | High – verified through signature and behavioral correlation                              |
| **Outcome**           | Suspicious processes successfully identified and terminated                               |

---

### 📊 **Output Interpretation**

| **Observation**             | **Analysis** | **Result**                                     |
| :-------------------------- | :----------- | :--------------------------------------------- |
| Unknown unsigned process    | Suspicious   | Possible malware detected                      |
| Running from temp folder    | Suspicious   | Not a system directory – needs review          |
| High CPU/memory usage       | Suspicious   | May indicate hidden malicious activity         |
| Valid signature in System32 | Trusted      | Legitimate system process                      |
| Network to unknown IP       | Suspicious   | Possible data leakage or malware communication |
| After removal and scan      | Clean        | System stable after cleanup                    |

<img width="1565" height="875" alt="Screenshot 2025-11-11 132250" src="https://github.com/user-attachments/assets/324b23bf-bfbd-4a83-a83b-18eddbc402fc" />


<img width="1919" height="994" alt="Screenshot 2025-11-11 132213" src="https://github.com/user-attachments/assets/37bef074-703e-4a89-ab1e-39889775b033" />

<img width="1914" height="993" alt="image" src="https://github.com/user-attachments/assets/ba8c8e04-49f1-4b13-8754-9c22c5f2b253" />

<img width="1448" height="1024" alt="image" src="https://github.com/user-attachments/assets/e557ac79-99d0-4884-9b22-412fc0ffcd6d" />





---

### ✅ **Conclusion**

Using **Process Explorer**, forensic analysts can effectively monitor, investigate, and validate system processes. The tool helps distinguish between trusted and malicious activities, ensuring system security and aiding in forensic investigations with high accuracy. 🕵️‍♀️
