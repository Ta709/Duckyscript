# Keychain Password Dump (Simulated) DuckyScript Payload

## Description
This DuckyScript payload is designed for macOS systems to simulate the dumping of saved passwords from the macOS Keychain using the built-in `security` command-line tool. It opens the Terminal app and runs a command that prompts the user for access to the keychain passwords.

This script is intended for **ethical hacking, red team exercises, and blue team detection training**. It helps security professionals understand suspicious behaviors and monitor for such activities.

## How it Works
- Opens the macOS Spotlight search.
- Launches the Terminal app.
- Runs the `security find-generic-password -wa ""` command to list generic keychain passwords.
- Exits Terminal.

> **Note:** The command requires the user's password or permission, so this is a simulation that highlights how an attacker might try to access saved passwords.
