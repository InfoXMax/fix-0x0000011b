<p align="center">
  <img src="https://your-image-url.com/cool-icon.png" alt="Icon">
</p>

# Windows Printer Error 0x0000011B Fix

> A registry script and troubleshooting guide to resolve printer-related issues on Windows.

## Table of Contents

- [Description](#description)
- [Problem](#problem)
- [Solution](#solution)
  - [Method 1: Restart Printer Spooler](#method-1-restart-printer-spooler)
  - [Method 2: Apply All Windows Updates](#method-2-apply-all-windows-updates)
  - [Method 3: Uninstall Recent Windows Updates](#method-3-uninstall-recent-windows-updates)
  - [Method 4: Manually Add the Printer Using Its IP Address](#method-4-manually-add-the-printer-using-its-ip-address)
  - [Method 5: Disable Print Spooler RPC Encryption (CVE-2021-1678 Fix)](#method-5-disable-print-spooler-rpc-encryption-cve-2021-1678-fix)
- [Contributing](#contributing)
- [License](#license)

## Description

The Windows printer error 0x0000011B is a bug found in Windows 11, 10, 8, and 7 operating systems. This error prevents your computer from connecting to a networked printer, affecting users attempting to connect to a shared printer or give a print command to a networked printer.

## Problem

The error may present itself with various messages, such as:
- "Windows cannot connect to the printer"
- "Operation failed with error 0x0000011B"
- "Add Printer: Windows cannot connect to the printer. Printer error 0x0000011B"

The issue is linked to the CVE-2021-1678 vulnerability security patch, which allowed hackers to exploit the Microsoft Remote Procedure Call (MSRPC) printer spooler to run malicious scripts remotely.

## Solution

This repository provides several methods to fix the printer error 0x0000011B. Please proceed with caution and consider creating a registry backup before making changes.

### Method 1: Restart Printer Spooler

An instant fix is to stop and restart the Printer Spooler process. Follow these steps:
1. Open the Task Manager using `Ctrl + Shift + Esc`.
2. Find and expand the "Spooler SubSystem App" process.
3. Right-click on the Printer Spooler task and choose "Open Services."
4. Stop the Printer Spooler service, then start it again.

### Method 2: Apply All Windows Updates

Ensure that your Windows system has all pending updates installed, as certain Windows Security updates may cause the issue.

### Method 3: Uninstall Recent Windows Updates

If the error started after installing specific Windows Security updates (e.g., KB5005565 and KB5005568), uninstalling those updates might help.

### Method 4: Manually Add the Printer Using Its IP Address

Remove the troubled printer and manually add it back using its hostname or TCP/IP protocol addresses.

### Method 5: Disable Print Spooler RPC Encryption (CVE-2021-1678 Fix)

If the error persists, consider disabling the CVE-2021-1678 fix by modifying the Registry Editor.

Please note that editing the registry comes with risks, so proceed with caution and ensure you know what you are doing.

For the detailed steps for each method, refer to the full troubleshooting guide in the article.

## Contributing

If you want to contribute to this project, follow these steps:
1. Fork the repository.
2. Create a new branch: `git checkout -b feature/my-feature`.
3. Make your changes and commit them: `git commit -m 'Add some feature'`.
4. Push the changes to your fork: `git push origin feature/my-feature`.
5. Submit a pull request.

Please ensure your pull request follows the [contribution guidelines](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](LICENSE).
