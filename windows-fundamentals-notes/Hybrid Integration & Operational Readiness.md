Week 4 — Hybrid Integration & Operational Readiness

1. Project Overview

This project demonstrates a basic Hybrid IT environment connecting a Windows virtual machine and a Kali Linux virtual machine through an isolated VMware Host-only network.

The project integrates operating systems, networking, SMB file sharing, access control, and Python automation.

2. Lab Architecture

          VMware Host-only Network
                     |
             +-------+-------+
             |               |
         Kali Linux       Windows 11
          (Client)         (Server)
             |               |
             +------ SMB ----+
                     |
                TCP Port 445
                     |
                Shared Folder

3. Network Configuration

Component| Configuration
Virtualization| VMware
Network Mode| Host-only
Windows OS| Windows 11
Linux OS| Kali Linux
Windows IP| 192.168.1.10
Kali IP| [Insert actual IP]

Both virtual machines were connected to the same virtual network.

4. Connectivity Testing

Network connectivity was verified using ICMP Ping between Windows and Kali Linux.

The test confirmed that both systems could communicate successfully.

5. SMB Service Testing

The SMB service was tested from Kali Linux.

Command:

nc -zv 192.168.1.10 445

Result:

Microsoft-ds 445 open

This confirmed TCP connectivity to the SMB service.

6. SMB Share Discovery

The following command was used:

smbclient -L //192.168.1.10 -U admin

Discovered shares included:

- ADMIN$
- C$
- IPC$
- nn
- Users

The custom share "nn" was accessed from Kali Linux using SMB client tools.

This demonstrated network-based resource access between Windows and Linux.

7. Security Concepts Demonstrated

The lab demonstrated the relationship between:

- Identity: The account requesting access.
- Authentication: Verifying the account's identity.
- Authorization: Determining permitted actions.
- Network: Providing connectivity between systems.
- Service: SMB providing file-sharing functionality.
- Resource: The shared folder and its contents.

8. Python Mini Automation

A Python File Classifier was developed.

The program classifies files according to their extensions and counts the number of files in each category.

Concepts used:

- Variables
- Lists
- Functions
- Conditions
- Loops
- Dictionaries
- String handling

The script executed successfully and generated a classification summary.

9. Security Observations

This lab illustrates several important security considerations:

1. Network exposure determines which systems can reach a service.
2. Open ports increase the available attack surface.
3. SMB authentication identifies the requesting account.
4. Share permissions and filesystem permissions influence resource access.
5. Administrative shares should be protected and exposed only when necessary.

10. Conclusion

This project integrated Windows, Linux, networking, SMB, access control, and Python automation into one practical environment.

It provided practical experience with a simplified Hybrid IT architecture and established a foundation for further Windows and Linux security studies.