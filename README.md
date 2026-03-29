# ActiveDirectory_Lab
This lab will simulate a real world enterprise environment using Active Directory domain services within a virtualised environment using Oracle's VirtualBox.

The lab consists of a Windows Server domain controller and a Windows client machine, configured to replicate common IT infrastructure scenarios such as user management, authentication, Group Policy enforcement, and network file sharing.

The hypervisor that is being used is virtual box on a Windows 11 system. A virtual Windows Server 2025 and Windows 11 system will be hosted to simulate the enterprise environment.

<img width="1900" height="1075" alt="OracleVM" src="https://github.com/user-attachments/assets/30ca2c3f-be63-4a78-8947-05eea6ce2d33" />

# Windows 2025 Server
Roles
- Active Directory Domain Services (AD DS)
- Domain Controller
- Vulnerability scanning host

# Windows 11 Client Machine
- Joined to domain

# Vulnerability Scanner
- Nessus will be used on Windows 2025 Server to scan Windows 11 client

# Network Setup
- NAT or Host-Only network
- Internal communication enabled

# Group Policy
Created and applied Group Policy Objects (GPOs)
- Password policies
- Security restrictions

# Host
The VMs 
