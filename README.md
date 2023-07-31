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

If you are certain that you are using a reliable antivirus for Windows 11, you may consider disabling the CVE-2021-1678 fix by modifying the Registry Editor. This method involves using the "fix-0x0000011b.reg" file provided in this repository.

**Warning**: Editing the registry comes with potential risks, so proceed with caution and ensure you understand the changes being made.

Here's how to use the "fix-0x0000011b.reg" file:

1. Download the [`fix-0x0000011b.reg`].

2. Double-click the downloaded `.reg` file to apply the changes to your registry.

3. If prompted, confirm the changes and allow the script to make modifications.

After applying the "fix-0x0000011b.reg" file and restarting your computer, try printing again and check if the issue is resolved. This registry script disables the RPC encryption for the Printer Spooler, which may help in fixing the "Printer error 0x0000011B" issue caused by the CVE-2021-1678 security patch.

Please remember to create a registry backup before making any changes, and ensure you have a reliable antivirus installed to protect your system from potential security risks.



## License

This project is licensed under the [MIT License](LICENSE).
