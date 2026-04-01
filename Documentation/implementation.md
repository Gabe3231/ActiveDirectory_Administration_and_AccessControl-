# Lab Implementation (Step-by-Step)

I began this lab by downloading the ISOs of the operating systems I would be using: Windows 11 Enterprise and Windows Server 2025. After obtaining the ISO, I initialized them in VirtualBox and assigned 3 CPU cores and about 8GB of RAM to ensure they ran smoothly. 

I began by setting up the Windows Server 2025

### Domain Controller Setup
On the Windows Server VM, I configured it to be the domain controller. 

Using the server manager application, I installed the Active Directory Domain Services (AD DS) role. Once it was installed, I promoted the server to a Domain Controller after creating a forest and domain named org.local. This was done because this role allows for the services required to manage identities and enforce centralized control in this simulated environment. (See Screenshots below)

A forest was created to create the hierarchical structure of Active Directory. This defines the boundary of the environment and allows users and admins to exist in a centralized directory. This is important as it allows admins to manage identities, permissions, and devices from a single location.

### User and Directory Configuration
After configuring the domain controller, I created user accounts within Active Directory using Active Directory Users and Computers (ADUC).

I originally crerated two users:
1. admin (administartive account)
2. USER-01 (Standard Domain User)
3. Gab (Third user added later for testing)

This was done to simulate an enterprise structure where IT admins have administrative access while regular users do not. This is important because authentication is done centrally rather than on each machine and allows admins to assign access control and other policies. This also allows multiple users to sign in to other devices using the same credentials as long as it's connected to the domain, which allows for scalability.

### Client Setup and Domain Join
After creating the domain, I had to then configure the Windows 11 Enterprise system to be a client on the network. I updated the clients' systems' DNS to point to the server's IPv4 address, which I set to static. This had to be done so the client could communicate and join the domain. After setting up, the client was joined to the domain org.local and used domain credentials.

This is important as it allows the client machine to become part of a centralized domain, authenticate users via the domain controller, and receive group policy configurations.

### File Share Config
After the client machine joined the domain, I configured a network file share to allow for centralized resource access and distribution. The folder was named Software on the server, and I configured the network resource using its path: \\WINDOWSSERVER\Software.

The folder was used to store MSI installation files for two software: Google Chrome and Zoom. This was done so they could later be deployed using Group Policy.

This is important because it allows machines joined to the domain to access shared resources from a single location. It also enables scalable software deployment without the need for manual installation. It also ensures security, as all machines within the group will be allowed to receive files from a controlled source.   

### Vulnerability Scanning
I incorporated the cybersecurity aspect into the lab using Nessus to scan the Windows 11 Enterprise client.

I simply identified the client machines' IP addresses via IPConfig and performed a targeted scan of them. 

Doing this allows admins to identify vulnerabilities and misconfigurations within the system while providing security insights into potential risks. This also shows how security tools are used to assess vulnerabilities and risks within an enterprise environment. 
