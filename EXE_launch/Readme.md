# USB Rubber Ducky Payload: `satan.exe` File Transfer and Execution

## 📄 Description

This payload transfers a file named `satan.exe` from a USB drive to the victim's computer, places it in the `%TEMP%` directory, and optionally executes it using PowerShell in a hidden window.

---

## 💻 Target

- Operating System: **Windows 10/11**
- Privileges: **Standard or Admin**
- Requirements: 
  - USB Rubber Ducky (or compatible HID injection device)
  - `satan.exe` on the root of USB (drive `E:` assumed)

---

## 🧠 Payload Behavior

1. Waits for 3 seconds to ensure the system is ready.
2. Opens the Run dialog (`Win + R`).
3. Launches PowerShell in hidden window mode.
4. Copies `satan.exe` from the USB to `%TEMP%`.
5. Executes `satan.exe`.
