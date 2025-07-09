# Decoy Ransomware Message with Detailed Skull ASCII Art (Green Text)

## Description
This DuckyScript payload opens the Windows Command Prompt and displays a large, detailed skull ASCII art along with a ransomware-style message. The text is shown in bright green on a black background, mimicking a ransom note to intimidate or prank the user. The Command Prompt remains open until a key is pressed.

This script is designed for **ethical hacking, red team exercises, and security awareness training**.

---

## How It Works
- Opens the Run dialog (`Win + R`).
- Launches `cmd.exe` (Command Prompt).
- Changes text color to bright green (`color 0A`).
- Prints a detailed skull ASCII art roughly centered.
- Displays the ransomware-style warning messages.
- Pauses the window to keep the message visible until user interaction.
