---
title: "Suspicious U.S.B Drive"
date: 2024-12-25
layout: post
---

## **Digital Forensics**

One of our clients informed us they recently suffered an employee data breach. As a startup company, they had a constrained budget allocated for security and employee training. I visited them and spoke with the relevant stakeholders. I also collected some suspicious emails and a USB drive an employee found on their premises. While I am analyzing the suspicious emails, can you check the contents on the USB drive?

**Challenge Submission**
Here were the objectives we needed to solve:

**What file is the autorun.inf running?**

**Does the PDF file pass the VirusTotal scan?**

**Does the file have the correct magic number?**

**What OS type can the file exploit?**

**A Windows executable is mentioned in the PDF file; what is it?**

**How many suspicious /OpenAction elements does the file have?**

## **Initial Analysis**
I was given the contents of the USB file and decided to first run it through **VirusTotal** for an external scan. VirusTotal flagged the ZIP folder as suspicious, with two files inside the archive identified as containing malware. The results indicated:

**VirusTotal Detection Results**

**Alibaba**: TrojanDropper:Win32/Meterpreter.e5f546e7
**Arcabit:** Trojan.CryptZ.Gen
**NANO-Antivirus:** Trojan.Script.Pidief.dugwyg
**Qihoo-360:** Pdf.launch.2.gen

From the names of the detected malware, I immediately noticed references to **Win32,** strongly suggesting that these files were designed to exploit the Windows OS.

## **Analyzing the autorun.inf File**
Next, I focused on analyzing the autorun.inf file. To extract and view its contents

**Unzipping the File:**
The ZIP file was password-protected. Using the provided password, I successfully extracted the files.

**Viewing autorun.inf:**
The file had an .inf extension, which can be opened directly or converted to a .txt file for easier reading. Inside, the contents revealed:
![ray-so-export](https://github.com/user-attachments/assets/382ef769-7511-4a0a-83bb-51090fd852d3)

This showed that the autorun.inf file was configured to execute the README.pdf file when the USB drive was accessed. The file being run is README.pdf.

## **Checking the PDF's Magic Number**
To verify if the PDF file had the correct magic number (a unique identifier at the start of the file that indicates its format), I used the macOS terminal:

**Command Used:**
![ray-so-export-2](https://github.com/user-attachments/assets/9666ffa8-3156-45a4-9d69-c69292a74fa0)

**Output:**
![ray-so-export-3](https://github.com/user-attachments/assets/1fc46e1d-7e6f-434f-a95f-2846a5a5435b)

This confirmed that the file's magic number (2550 4446 = %PDF) was valid for a PDF, specifically version 1.7. The PDF was correctly identified as a valid document.

## **Does the File Pass VirusTotal?**
After confirming the file's validity, I uploaded the README.pdf file to VirusTotal. It was flagged by one vendor (NANO-Antivirus) as containing a Trojan:

**Detection Name:** Trojan.Script.Pidief.dugwyg
The file’s malicious intent was evident, but since it was only flagged by one vendor, the threat could be narrowly targeted.

## **Exploring Suspicious Actions in the PDF**
To further investigate the malicious behavior of the PDF, I used Hex Fiend (a hex editor for macOS) to inspect the file’s structure.

Searching for **/OpenAction:**

Using Hex Fiend’s search function, I located an **/OpenAction** element pointing to object 27 in the PDF.
The **/OpenAction** directive is often used in malicious PDFs to automatically execute commands or scripts when the file is opened.

**Object 27 Analysis:**
The object revealed a /Launch command designed to execute:
![ray-so-export-4](https://github.com/user-attachments/assets/ce91e71a-ff36-4f6b-b9cd-6c6c12235888)

**This command attempts to:**

Launch the Windows Command Prompt **(cmd.exe).**

**Navigate directories** (e.g., Desktop, Documents, Escritorio) to locate and open the README.pdf file.
This confirmed the malicious behavior of the PDF, which was engineered to exploit Windows systems.
How Many Suspicious /OpenAction Elements?
From the Hex Fiend analysis:

**Finding /OpenAction:** Only one /OpenAction element was found in the PDF.

This single action was responsible for triggering the execution of **cmd.exe.**
**Conclusion:** The PDF contained one suspicious /OpenAction element.

## **Summary of Findings**
**File Executed by autorun.inf:** README.pdf

**Does the PDF Pass VirusTotal?:** No, flagged by NANO-Antivirus.

**Correct Magic Number:** Yes, %PDF-1.7.

**OS Targeted:** Windows.

**Windows Executable Mentioned:** cmd.exe.

**Suspicious /OpenAction Elements:** One.

$$ **Conclusion**
This investigation showcased the risks of suspicious files on USB drives. By combining tools like VirusTotal, Hex Fiend, and macOS terminal commands, I successfully identified the malicious intent and behavior of the files. This reinforces the importance of robust endpoint protection and training for employees to handle USB devices and suspicious emails cautiously.








