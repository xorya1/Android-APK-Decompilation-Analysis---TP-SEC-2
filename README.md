# Android APK Decompilation & Analysis - TP SEC 2

**Author:** Alaoui Belghiti Hanaa  
**Class:** SICS4

---

## Project Overview
This project is part of a practical exercise (TP) focused on decompiling an Android APK, analyzing its structure, modifying parts of the code, and re-signing the APK. The main goal is to explore key Android security concepts such as file analysis, reverse engineering, and APK modifications.

For detailed explanations and specific command examples, refer to the accompanying TP document.

---

## Table of Contents
1. [Exercise 1: APK Decompilation & Recompilation](#exercise-1-apk-decompilation--recompilation)
2. [Exercise 2: Analyzing .odex and .oat Files](#exercise-2-analyzing-odex-and-oat-files)
3. [Exercise 3: Modifying APK to Hide Sensitive Information](#exercise-3-modifying-apk-to-hide-sensitive-information)
4. [Conclusion](#conclusion)

---

## Exercise 1: APK Decompilation & Recompilation

### Description:
In this exercise, I worked on an Android app in Android Studio, located the `app-debug.apk`, and decompressed it using 7-Zip and Apktool. I made changes to the APK, recompiled, signed, and tested it on an emulator.

### Steps:
1. Launch the app in Android Studio and locate the APK.
2. Decompress the APK using 7-Zip.
3. Open `classes.dex` in Jadx to compare it with the original code.
4. Check the `AndroidManifest.xml` file after decompression.
5. Recompile and sign the APK using Apktool and command-line tools.
6. Deploy the recompiled APK on the emulator.

For more details and exact commands used, refer to the TP document.

---

## Exercise 2: Analyzing .odex and .oat Files

### Description:
This exercise focuses on analyzing Android's `.odex` and `.oat` files, understanding how applications are optimized, and retrieving data for further analysis.

### Steps:
1. Use `adb shell` to navigate the Android shell and list app packages.
2. Locate and copy the `base.odex` file from the device to the computer.
3. Analyze `base.odex` using `objdump` and compare it with the `boot-ext.oat` file.
4. Use the `baksmali` tool to read the `.odex` file (issue encountered, switch to `readelf` for successful analysis).

For full command details and issues encountered, check the TP document.

---

## Exercise 3: Modifying APK to Hide Sensitive Information

### Description:
In this exercise, I identified a security flaw where the password was exposed in the logcat output. I modified the APK to hide the password and ensured that the modified APK works correctly.

### Steps:
1. Capture the logcat output displaying the password.
2. Decompress the `app-release.apk` and modify the `MainActivity` code to hide the password.
3. Recompile and sign the modified APK.
4. Replace the original APK on the emulator with the modified version.
5. Verify that the password is no longer visible in the logs.

A more detailed explanation of the modifications and steps taken can be found in the TP document.

---

## Conclusion
This project provided practical insights into APK decompilation, reverse engineering, and Android security. Through these exercises, I gained a deeper understanding of Android’s internal structure and how to mitigate potential security risks by modifying APKs.

For further information and in-depth technical details, please refer to the accompanying TP document.



