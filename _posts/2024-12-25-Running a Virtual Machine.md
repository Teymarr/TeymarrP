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


