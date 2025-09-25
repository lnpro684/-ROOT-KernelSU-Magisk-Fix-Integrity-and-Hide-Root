# Root Module Hiding & Play Integrity Fix 🛡️

This project provides a comprehensive solution for users who need to maintain device integrity and bypass checks that are often triggered by a rooted Android device. It combines advanced **root hiding** techniques with the implementation of a **Play Integrity Fix**, allowing applications and services that rely on device authenticity to function correctly.

---

### 📋 Table of Contents

-   [What is Play Integrity?](#what-is-play-integrity)
-   [Why Do We Need to Hide Root?](#why-do-we-need-to-hide-root)
-   [How Does This Fix Work?](#how-does-this-fix-work)
-   [Features](#features)
-   [Prerequisites](#prerequisites)
-   [Installation & Usage](#installation--usage)
-   [Disclaimer](#disclaimer)

---

### What is Play Integrity?

Google's **Play Integrity API** is a security measure designed to protect apps and games from fraud, abuse, and piracy. It provides a response that helps determine whether you're interacting with a genuine Android device, whether the app is a legitimate version, and whether the user is a real human. When a device is rooted, it often fails these checks, preventing certain applications (like banking apps, streaming services, and some games) from running.

### Why Do We Need to Hide Root?

While rooting an Android device offers many benefits, such as full control over the system, it also introduces security vulnerabilities. Many applications and services have built-in **root detection** mechanisms to prevent potential security risks. The primary purpose of **root hiding** is to make the device appear unrooted to these applications, allowing them to run without issues.

### How Does This Fix Work?

This solution leverages a combination of a **Magisk** module and a custom `play_integrity_fix.sh` script to achieve its goals.

1.  **Magisk Module:** The core of the root hiding is a custom Magisk module that manipulates the system partition. It works by altering key files and properties to deceive apps that perform root checks.
2.  **Play Integrity Fix Script:** The included script automates the process of spoofing device fingerprints to pass Google's Play Integrity checks. It fetches a valid fingerprint from a certified device and applies it to your system, tricking the Play Integrity API into thinking your device is a trusted one.

### Features

-   **Seamless Root Hiding:** Hides the presence of root from a wide range of applications.
-   **Automated Play Integrity Fix:** Automatically updates the necessary device fingerprints to pass the latest integrity checks.
-   **Easy to Install:** Can be easily installed via **Magisk**.
-   **Active Community Support:** Backed by an active community for updates and troubleshooting.

### Prerequisites

-   A rooted Android device.
-   [**Magisk**](https://github.com/topjohnwu/Magisk) or [**KernelSU**](https://github.com/tiann/KernelSU) installed.
-   [**Play Integrity API Checker**](http://play.google.com/store/apps/details?id=gr.nikolasspyr.integritycheck&hl=id&pli=1) Installed for checking device integrity.

### Installation & Usage

1.   Download the all the module from the releases page.
2.   Make sure you downloaded the compatible module for your android version, or just use recomendation on releases page.
3.   Open the root app and go to the "Modules" section.
4.   Tap "Install from storage," locate the downloaded zip file, and select it.
5.   Before you reboot, get back and flash another module until all is flashed into your root app.
6.   Magisk will flash the module. Once complete, **reboot your device**.
7.   After reboot,
     - If you are using Magisk, go open KSUWebui and click at "Play Integrity Fix [Inject]",  click advanced and check all exept the top one and the bottom one.
     - If you are using KernelSU, open the app, click at "Play Integrity Fix [Inject]",  click advanced and check all exept the top one and the bottom one.
8.   Reboot again,
     - If you are using Magisk, go open KSUWebui and click at "Tricky Store",  click 3 bars at the top, select all, diselect unnecessary, set valid keybox, set security patch, and save.
     - If you are using KernelSU, open the app, click at "Tricky Store", click 3 bars at the top, select all, diselect unnecessary, set valid keybox, set security patch, and save.
9.   The fix will be active. You can verify its status using a **Play Integrity API Checker** application. But to hide your root, get to number 10 and next
10.  Reboot again, check the notification, click the "LSposed" and go to module, activate the "Hide My Applist".
11.  Reboot again, open "Hide My Applist" app and select "App Manage", select your app that you need to hide from root to working properly.
12.  At the app setting check the work mode.
13.  Reboot again, and hide the magisk app, and also configure denylist for app that you hide.
14.  Last Reboot. It your app will work properly.

### Disclaimer

This project is intended for educational purposes only. The authors are not responsible for any damage to your device or any legal issues that may arise from using this software. Using this fix may violate the terms of service of certain applications. Use at your own risk.
