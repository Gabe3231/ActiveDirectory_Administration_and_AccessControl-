# Completed Objectives
1. Set up a Windows Server 2025, promoted it to a Domain Controller, and set up Active Directory Domain Services with a domain titled org.local.
2. Provisioned a virtual Windows 11 Enterprise client and created two domain users: admin and USER-01.
3. Joined the client machine (USER-01) to the domain and authenticated using the domain credentials.
4. Created and applied Group Policy Objects (GPOs) to automate app software installation (Google Chrome and Zoom).
5. Utilized Nessus to scan the client (USER-01) and generate a network scan report for security remediation planning.

## Overview
This lab will simulate a real-world enterprise environment using Active Directory domain services within a virtualized environment using Oracle's VirtualBox.

The lab consists of a Windows Server domain controller and a Windows client machine, configured to replicate common IT infrastructure scenarios, including user management, authentication, Group Policy enforcement, and network file sharing.

## Lab Environment

The hypervisor is running on a Windows 11 system with an i5 12600KF and 32GB of DDR4 RAM. The operating systems being hosted are Windows Server 2025 and Windows 11 Enterprise. Each has been allocated 3 cores and 8GB of RAM.

<img width="1919" height="1079" alt="Screenshot 2026-03-29 104026" src="https://github.com/user-attachments/assets/526a54a3-beed-4f27-867a-c333c4922675" />

# Lab Implementation (Step-by-Step)

I began this lab by downloading the ISOs of the operating systems I would be using: Windows 11 Enterprise and Windows Server 2025. After obtaining the ISO, I initialized them in VirtualBox and assigned 3 CPU cores and about 8GB of RAM to ensure they ran smoothly. 

I began by setting up the Windows Server 2025

### Domain Controller Setup
On the Windows Server VM, I configured it to be the domain controller. 

Using the server manager application, I installed the Active Directory Domain Services (AD DS) role. Once it was installed, I promoted the server to a Domain Controller after creating a forest and domain named org.local. This was done because this role allows for the services required to manage identities and enforce centralized control in this simulated environment. (See Screenshots below)

A forest was created to create a hierarchical structure of Active Directory. This defines the boundary of the environment and allows users and admins to exist in a centralized directory. By doing this, I created a new Active Directory.


# Screenshots / System Configuration

### Windows Server 2025 - Domain Controller Setup
- Active Directory Domain Services (AD DS)
<img width="1431" height="1005" alt="domainCreation" src="https://github.com/user-attachments/assets/1cfff535-96b0-4e22-87ed-a9008f0ef71e" />
<img width="1439" height="1005" alt="part2" src="https://github.com/user-attachments/assets/8d888b1e-6e3b-4aa0-8dd7-6479afd3ce92" />
<img width="1436" height="1002" alt="domainCreation2" src="https://github.com/user-attachments/assets/a6c8e816-d128-4aee-a7db-37ebef55cb88" />
<img width="1438" height="1005" alt="art3" src="https://github.com/user-attachments/assets/89fb28b8-06a5-406a-9bff-cf38e3d5308f" />
<img width="1439" height="1006" alt="part4" src="https://github.com/user-attachments/assets/993038a8-df8d-4f3a-a492-665e61bc4a1e" />
<img width="1438" height="1002" alt="part5" src="https://github.com/user-attachments/assets/30688619-3e78-4fca-b3b1-c5828bec39b7" />


- Domain Controller
<img width="1743" height="1079" alt="Screenshot 2026-03-28 231334" src="https://github.com/user-attachments/assets/a73efa5c-a143-43df-8714-de1ca1b194b5" />


- Vulnerability scanning host

### Enterprise Windows 11 Client Machine
- Joined the domain
<img width="1919" height="1079" alt="BothVMs" src="https://github.com/user-attachments/assets/a7466145-4843-4f65-8098-31466f2f431b" />
<img width="1919" height="1079" alt="DomainJoin" src="https://github.com/user-attachments/assets/b154f6d6-65aa-498d-b6de-dd4f25d868c6" />

### Vulnerability Scanner
- Nessus will be used on Windows 2025 Server to scan Windows 11, client
<img width="1919" height="1079" alt="Screenshot 2026-03-29 140441" src="https://github.com/user-attachments/assets/e0cecf8a-8817-46e8-b2d8-7a2990429089" />
<img width="1919" height="1079" alt="Screenshot 2026-03-29 140921" src="https://github.com/user-attachments/assets/132b1121-f6cb-4099-840b-57c5bea12244" />


### Network Setup
- Adapter 1: NAT
- Adapter 2: Internal Network

### Group Policy
- Designed and implemented Group Policy Objects (GPOs) to automate software deployment
<img width="1919" height="1079" alt="MSI" src="https://github.com/user-attachments/assets/57fa578b-33e1-41a5-ba7c-56aca9b045ad" />
<img width="1919" height="1079" alt="AppInstall" src="https://github.com/user-attachments/assets/eabd1353-1a87-45c3-a4a9-05ed61082c04" />
<img width="1919" height="1079" alt="policyFiles" src="https://github.com/user-attachments/assets/39808add-a411-4f0f-9f22-a1bbcffd8ed7" />

