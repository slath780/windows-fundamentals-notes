


1. Lab Objective

Build an isolated hybrid environment where a Linux VM communicates with a Windows VM and accesses a shared resource using SMB.

2. Lab Architecture

             Internal Virtual Network
                       |
              ┌────────┴────────┐
              |                 |
           Linux VM          Windows VM
           SMB Client        SMB Server
              |                 |
              └──── TCP/445 ────┘
                       |
                 Shared Folder

3. Environment

Component| Configuration
Linux OS| [Distribution and version]
Windows OS| [Version]
Virtualization| [VMware / VirtualBox]
Network Mode| [Internal / Host-only]
Linux IP| [Actual lab IP]
Windows IP| [Actual lab IP]

4. Network Configuration

Document the network interfaces and IP configuration of both virtual machines.

Linux:

- Interface: [Actual interface]
- IP Address: [Actual IP]

Windows:

- Interface: [Actual interface]
- IP Address: [Actual IP]

5. Connectivity Testing

Record the results of testing communication between the two systems.

Test| Result
Linux to Windows connectivity| [Success / Failure]
Windows to Linux connectivity| [Success / Failure]
TCP port 445 accessibility| [Verified / Not verified]

Evidence:
[Add relevant command output or screenshots]

6. SMB Configuration

Windows was configured to provide a test shared folder.

- Share Name: [Actual share name]
- Shared Folder Path: [Actual path]
- SMB Service Status: [Actual status]
- Network Share Path: [Actual UNC path]

7. Authentication and Authorization

Document the account used by the Linux client to access the SMB share.

- Account: [Test account]
- Authentication Result: [Success / Failure]
- Access Level: [Read / Write / Modify]
- Authorization Result: [Allowed / Denied]

8. Security Testing

Record the access-control tests performed.

Test| Expected Result| Actual Result
Authorized user accesses share| Allow| [Result]
Unauthorized user accesses share| Deny| [Result]
Read operation| According to permissions| [Result]
Write operation| According to permissions| [Result]

9. Observations

Document:

- Network connectivity issues.
- Authentication behavior.
- Permission-related failures.
- Relevant Windows events.
- Any troubleshooting performed.

10. Conclusion

Summarize what the lab demonstrated about:

- Linux and Windows communication.
- SMB-based file sharing.
- Authentication.
- Authorization.
- Network resource access.
