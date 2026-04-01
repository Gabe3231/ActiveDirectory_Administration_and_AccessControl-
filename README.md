# Active Directory Lab

## Completed Objectives
1. Set up a Windows Server 2025, promoted it to a Domain Controller, and set up Active Directory Domain Services with a domain titled org.local.
2. Provisioned a virtual Windows 11 Enterprise client and created two domain users: admin and USER-01.
3. Joined the client machine (USER-01) to the domain and authenticated using the domain credentials.
4. Created and applied Group Policy Objects (GPOs) to automate app software installation (Google Chrome and Zoom).
5. Utilized Nessus to scan the client (USER-01) and generate a network scan report for security remediation planning.

### Overview
This lab will simulate a real-world enterprise environment using Active Directory domain services within a virtualized environment using Oracle's VirtualBox.

The lab consists of a Windows Server domain controller and a Windows Enterprise client machine, configured to replicate common IT infrastructure scenarios, including user management, authentication, Group Policy enforcement, and network file sharing.

### Lab Environment

The type 2 hypervisor is running on a Windows 11 system with an i5 12600KF and 32GB of DDR4 RAM. The operating systems being hosted are Windows Server 2025 and Windows 11 Enterprise. Each has been allocated 3 cores and 8GB of RAM.

<img width="1919" height="1079" alt="Screenshot 2026-03-29 104026" src="https://github.com/user-attachments/assets/526a54a3-beed-4f27-867a-c333c4922675" />

## Documentation

- [Implementation Walkthrough](implementation.md](https://github.com/Gabe3231/ActiveDirectory_Administration_and_AccessControl-/blob/main/README.md#:~:text=implementation.md)](https://github.com/Gabe3231/ActiveDirectory_Administration_and_AccessControl-/blob/main/Documentation/implementation.md))
- [Screenshots / System Configuration](Screenshots.md](https://github.com/Gabe3231/ActiveDirectory_Administration_and_AccessControl-/edit/main/README.md#:~:text=screenshots.md))

## Skills Demonstrated

- Active Directory Domain Services (AD DS)
- Domain Controller configuration
- Centralized user and device management
- DNS and domain join configuration
- Group Policy Object (GPO) deployment
- Network file sharing
- Vulnerability scanning with Nessus
- Virtualization using Oracle VirtualBox

