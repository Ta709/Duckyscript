# Windows Defender Disabler/Restorer (English Windows 10/11)

## Overview

This DuckyScript payload is designed to automate the process of disabling or restoring Windows Defender on **English-language Windows 10/11** machines. It attempts to first disable Windows Defender's **Tamper Protection** via GUI navigation and then executes PowerShell commands to disable various other Defender features and modify relevant registry keys. It also includes a function to restore Defender to its default state.

**Author:** HackingMark (Original Concept)
**Adapted by:** Me :)
**Version:** 1.1 (English Adaptation)
**Target OS:** English Windows 10/11 (22H2 recommended for original version)

## **⚠️ CRITICAL WARNINGS & DISCLAIMER ⚠️**

* **ETHICAL USE ONLY:** This script is provided for **educational purposes and authorized security testing ONLY**. Using this script on any system you do not own or have explicit, legal authorization to test on is **ILLEGAL and UNETHICAL**. Respect privacy and system integrity.
* **ADMINISTRATOR PRIVILEGES REQUIRED:** The PowerShell commands within this script require administrative privileges. The script attempts to open an elevated PowerShell window. If User Account Control (UAC) is configured to require a password for elevation, this script **WILL FAIL** at the UAC prompt.
* **TAMPER PROTECTION:** On modern Windows versions (Windows 10 1903+ and Windows 11), **Tamper Protection** is enabled by default. This feature is designed to prevent malicious software (and scripts like this) from altering Windows Defender settings. While this script *attempts* to disable Tamper Protection via GUI navigation, the success of this step is **highly fragile** and can fail due to:
    * **UI Changes:** Microsoft frequently updates the Windows Security interface. The exact sequence of `TAB` presses required to navigate the GUI is very sensitive to these changes, Windows version, build number, and even window size/focus.
    * **UAC Prompts:** Confirming the Tamper Protection change involves a UAC prompt, which the script attempts to bypass with `ALT Y`. This may not always work depending on the prompt's focus or if a password is required.
* **DETECTION:** Even if successful, modern Antivirus (AV) and Endpoint Detection and Response (EDR) solutions are highly likely to detect the execution of these commands as suspicious or malicious behavior. This is not a "stealthy" operation.
* **UNRELIABILITY:** Due to the reliance on GUI automation and the moving target of Windows security features, this script's reliability is not guaranteed across all Windows 10/11 versions and configurations. **Thorough testing on your specific target system is essential.**

## How to Use

1.  **Save the Code:** Copy the DuckyScript code below into a file named `payload.txt` (or whatever your DuckyScript compiler expects).
2.  **Choose Mode:** At the very end of the script, uncomment **either** `DISABLE_WINDOWS_DEFENDER()` or `RESTORE()` based on your desired action.
    * `DISABLE_WINDOWS_DEFENDER()`: To attempt to turn off Windows Defender.
    * `RESTORE()`: To attempt to turn Windows Defender back on.
3.  **Compile & Load:** Use your DuckyScript compiler to convert `payload.txt` into a `.bin` file, and load it onto your USB Rubber Ducky (or compatible HID device like a LilyGO T-Dongle S3).
4.  **Execute:** Plug the HID device into your target Windows 10/11 machine.
