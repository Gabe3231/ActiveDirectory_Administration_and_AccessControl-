# Completed Objectives
1. Setup a virtual Windows 2025 Server and setup Active Directory Domain Services with a domain titled org.local
2. Provisioned a virtual Enterprise Windows 2025 clinet and created two domain users: admin and USER-01
3. Joined client machine (USER-01) to the domain and authticated using domain credentials
4. Created and applied Group Policy Objects (GPOs) on what apps 

# ActiveDirectory_Lab
This lab will simulate a real world enterprise environment using Active Directory domain services within a virtualised environment using Oracle's VirtualBox.

The lab consists of a Windows Server domain controller and a Windows client machine, configured to replicate common IT infrastructure scenarios such as user management, authentication, Group Policy enforcement, and network file sharing.

The hypervisor that is being used is virtual box on a Windows 11 system. A virtual Windows Server 2025 and Windows 11 system will be hosted to simulate the enterprise environment.

<img width="1900" height="1075" alt="OracleVM" src="https://github.com/user-attachments/assets/30ca2c3f-be63-4a78-8947-05eea6ce2d33" />

# Windows 2025 Server
Roles
- Active Directory Domain Services (AD DS)
<img width="1436" height="1002" alt="domainCreation2" src="https://github.com/user-attachments/assets/a6c8e816-d128-4aee-a7db-37ebef55cb88" />
<img width="1431" height="1005" alt="domainCreation" src="https://github.com/user-attachments/assets/1cfff535-96b0-4e22-87ed-a9008f0ef71e" />
- Domain Controller
<img width="1743" height="1079" alt="Screenshot 2026-03-28 231334" src="https://github.com/user-attachments/assets/a73efa5c-a143-43df-8714-de1ca1b194b5" />
- Vulnerability scanning host

# Enterprise Windows 11 Client Machine
- Joined to domain
<img width="1919" height="1079" alt="DomainJoin" src="https://github.com/user-attachments/assets/b154f6d6-65aa-498d-b6de-dd4f25d868c6" />
<img width="1919" height="1079" alt="BothVMs" src="https://github.com/user-attachments/assets/a7466145-4843-4f65-8098-31466f2f431b" />

# Vulnerability Scanner
- Nessus will be used on Windows 2025 Server to scan Windows 11 client

# Network Setup
- Adapter 1: NAT
- Adapter 2: Internal Network

# Group Policy
- Created and applied Group Policy Objects (GPOs) (Instalation Policy)
<img width="1919" height="1079" alt="AppInstall" src="https://github.com/user-attachments/assets/eabd1353-1a87-45c3-a4a9-05ed61082c04" />
<img width="1919" height="1079" alt="MSI" src="https://github.com/user-attachments/assets/57fa578b-33e1-41a5-ba7c-56aca9b045ad" />
<img width="1919" height="1079" alt="policyFiles" src="https://github.com/user-attachments/assets/39808add-a411-4f0f-9f22-a1bbcffd8ed7" />
- Password policies
- Security restrictions

