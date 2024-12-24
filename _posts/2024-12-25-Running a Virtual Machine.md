---
title: "Running a Virtual Machine (VM)"
date: 2024-12-25
layout: post
---
Hello everyone, Teymarr here! Today, I’m recounting my full experience setting up a Windows on ARM virtual machine (VM) on my Apple Silicon (M2) Mac. I started with UTM, navigated through numerous dependency hurdles, removed references to chntpw, and overcame unexpected folder-structure issues. In the end, I successfully created a working Windows on ARM ISO using UUP Dump. Below is the detailed blog post capturing every twist and turn along the way.

## **Why Run Windows on ARM on an M2 Mac?**

Experimentation & Learning: Especially in cybersecurity, it’s useful to have multiple operating systems at your disposal for testing.
ARM Architecture: Apple’s M2 chip means we need ARM-based OS images rather than traditional x86.
Isolation: Using a VM preserves my primary macOS environment while still giving me a place to install and test Windows.

## **Tools & Software**

**UTM**: A popular virtualization/emulation tool for macOS, particularly for M1/M2.

**UUP Dump**: An online resource for building a Windows on ARM ISO.

**Homebrew**: The package manager for macOS to install command-line tools.

## **Step 1**: Installing UTM

**Download UTM**:
I grabbed UTM from https://mac.getutm.app

**Move UTM to Applications**:
Drag-and-drop the .app file into Applications to install.

**Open UTM**:
If macOS warns you about an unidentified developer, go to System Settings → Privacy & Security and click “Open Anyway.”

## **Step 2: Obtaining a Windows on ARM ISO via UUP Dump**
Traditional Windows ISOs (for x86) won’t run natively under Apple Virtualization on M2, so I needed a **Windows on ARM image**.

## **2.1 Download the UUP Dump Scripts**
1. Visit https://uupdump.net
2. Select an ARM64 build of Windows 10/11 (I chose Windows 11).
3. I selected the arm64 for the most recent publicly released build.
4. Download the .zip archive containing scripts (e.g., uup_download_macos.sh) and extraction tools.

## 2.2 Extract the Scripts
1. Unzip the downloaded folder (mine was named 26100).
   
2. Navigate to it in Terminal:
![Bash](https://github.com/user-attachments/assets/88aa937e-4bd0-450c-8876-1be88db902a6)

## Step 3: Installing Dependencies via Homebrew
When I first ran the script, I kept hitting errors about missing tools. UUP Dump needs several dependencies:
I already have homebrew installed, so I decided to see if I could batch install everything.

1. **Install Required Packages**
![Bash](https://github.com/user-attachments/assets/5c24aa1f-0a60-4bbd-bb95-635f7d1ec0a7)

**aria2** – Parallel file downloader

**cabextract** – Extracts Microsoft .cab files

**wimlib** (includes wimlib-imagex) – Handles .wim Windows images

**cdrtools** (includes mkisofs) – Creates the final ISO

**Note**: The script also checks for chntpw, but that’s no longer in the main Homebrew repositories. It isn’t strictly required for building the ISO.


## Step 4: Bypassing the chntpw Check
**4.1 Editing the Script**
The script initially stops if it can’t find chntpw. To skip that:

1. **Open the script in Nano**
   ![Bash-2](https://github.com/user-attachments/assets/9960bf48-f773-4224-a1c7-affab1eb97bd)

2. **Locate the dependency check near the top**:
   ![Bash-3](https://github.com/user-attachments/assets/96b37853-b4dc-4219-875b-be4aec57feb4)

3. **Remove "chntpw" from that list**:
   ![Bash-4](https://github.com/user-attachments/assets/9adb2c6b-84ac-44e8-9e29-1bd3ff770083

4. **Save and Exit**:
   Press **Ctrl+O**, then **Enter** to save.
   Press **Ctrl+X** to exit Nano.

   


