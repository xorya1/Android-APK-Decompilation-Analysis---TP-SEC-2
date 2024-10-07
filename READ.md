Android APK Decompilation & Analysis - TP SEC 2
Author: Alaoui Belghiti Hanaa
Class: SICS4
Project Overview
This project is part of a practical exercise (TP) aimed at demonstrating the process of decompiling an Android APK, analyzing its structure, modifying specific parts of the code, and re-signing the APK for testing. The TP focuses on key Android security concepts such as file analysis, reverse engineering, and APK modifications.

For more detailed explanations and specific command examples, please refer to the provided TP document.

Table of Contents
Exercise 1: APK Decompilation & Recompilation
Exercise 2: Analyzing .odex and .oat Files
Exercise 3: Modifying APK to Hide Sensitive Information
Exercise 1: APK Decompilation & Recompilation
Description:
In this exercise, I launched an Android application in Android Studio, located the app-debug.apk, and decompressed it using different tools (7-Zip and Apktool). After making some modifications, I recompiled and signed the APK before running it on an emulator.

Steps:

Launching the app in Android Studio and finding the APK.
Decompressing the APK with 7-Zip.
Opening classes.dex in Jadx to compare it with the original code.
Checking the contents of AndroidManifest.xml after decompression.
Recompiling and signing the APK using Apktool and command-line signing tools.
Deploying the newly signed APK to the emulator for testing.
For more details on each step and commands used, please refer to the TP document.

Exercise 2: Analyzing .odex and .oat Files
Description:
This exercise explores the analysis of Android's .odex and .oat files, which are important for understanding how Android applications are optimized and stored on devices.

Steps:

Navigating the Android shell with adb shell and listing app packages.
Locating and copying base.odex from the device to the local machine.
Analyzing base.odex using objdump and comparing it with boot-ext.oat.
Attempting to read the .odex file using baksmali and switching to readelf for successful analysis.
Complete command explanations and issues encountered can be found in the TP document.

Exercise 3: Modifying APK to Hide Sensitive Information
Description:
In this final exercise, I identified a security flaw where the password was exposed in the application logs. I modified the APK to hide the password and ensured the changes were correctly applied by testing the modified APK.

Steps:

Capturing logcat output that displayed the password.
Decompressing app-release.apk and modifying MainActivity to hide the password.
Recompiling the modified APK and signing it.
Replacing the original APK with the modified version on the emulator.
Verifying that the password was no longer visible in the logs.
A detailed walkthrough of how the password was hidden and how the APK was modified is available in the TP document.

Conclusion
This project provided practical insights into the processes of APK decompilation, reverse engineering, and mobile application security. The exercises enhanced my understanding of Android's inner workings and how to mitigate security risks by modifying APKs.

For further information and in-depth technical explanations, please refer to the TP document accompanying this README