# SMB Enumeration Lab: Information Gathering & Share Analysis

## Project Overview
This project serves as a practical lab exercise focused on enumerating and analyzing Server Message Block (SMB) services on a vulnerable target (Metasploitable 2). The primary objective is to demonstrate how attackers gather critical system information, map local users, identify exposed network shares, and exploit misconfigurations such as anonymous (Null Session) logins.

Through this exercise, practitioners learn to transition from automated enumeration to manual interaction, testing both share-level and filesystem-level permissions.

## Objectives
* Perform comprehensive SMB enumeration to discover shares, users, and OS details.
* Identify misconfigured shares allowing anonymous access.
* Manually interact with target shares using SMB protocols.
* Validate read/write permissions to understand the difference between share access and underlying Linux filesystem permissions.

## Tools Utilised
* **enum4linux:** For automated extraction of user lists, share lists, and OS fingerprinting.
* **smbclient:** For interactive, FTP-style connection and manipulation of SMB/CIFS resources.

## Environment Setup
* **Attacker System:** Kali Linux VM
* **Target System:** Metasploitable 2 VM (IP: `192.168.1.16` or your specific lab IP)
* **Network:** Isolated Host-Only Lab Network

## Methodology
1. **Initial Enumeration:** Running `enum4linux` to map out the target's SMB configuration.
2. **Anonymous Verification:** Using `smbclient` with the `-N` (No Password) flag to list shares anonymously.
3. **Share Interaction:** Connecting to vulnerable shares (e.g., `tmp`) via null sessions.
4. **Permission Testing:** Attempting to read existing files and upload new files to test for unauthorised read/write access.

## Disclaimer
**Educational Purposes Only.** This lab and the accompanying documentation are designed strictly for educational and training purposes. All activities were conducted in a safely isolated, local lab environment. Never attempt to enumerate or exploit systems without explicit, documented permission from the owner.
