# AZURE AD LAB
---
## 📘 Overview
This project demonstrates how to deploy a **mini Active Directory environment in Azure** using two virtual machines.
It’s designed for training and demonstration — showing how a Windows Server domain, client join, and Group Policies work together.
**Key Components**
- **DC01:** Windows Server 2019 (AD DS, DNS, DHCP)
- **CLIENT01:** Windows 11 Pro (domain joined)
- **Network:** Azure Virtual Network + Network Security Group (NSG)
- **Access:** Direct RDP (no Bastion, low cost)
---
## 🧠 Learning Objectives
- Understand how **Active Directory** manages users and computers
- See how **Azure Fabric DHCP** differs from on-prem DHCP
- Apply **Group Policy Objects (GPOs)** for control and security
- Demonstrate **RDP security and centralized management**
- Learn how a single server can manage multiple users and machines
---
## ⚙️ Core Lab Setup
| Component | Purpose | Notes |
|------------|----------|-------|
| **Resource Group** | Container for all Azure assets | Deleted to clean up everything at once |
| **Virtual Network (VNet)** | Private IP network (192.168.100.0/24) | Simulates an internal LAN |
| **Network Security Group (NSG)** | Firewall to limit inbound RDP | Allows only instructor’s IP on port 3389 |
| **DC01 (Server)** | Domain Controller | Runs AD DS, DNS, optional DHCP |
| **CLIENT01 (Workstation)** | Domain-joined client | Used for user login and GPO testing |
---
## 🪄 Key Group Policies Demonstrated
| GPO | Purpose | Result |
|-----|----------|--------|
| **Disable Control Panel** | Restrict system access | Users see “Restricted by your administrator” |
| **Prevent Wallpaper Change** | Enforce shared wallpaper | Company logo appears on all desktops |
| **Remove Task Manager** | Prevent task termination | Ctrl + Alt + Del → Task Manager greyed out |
| **Allow RDP for Students** | Enable remote login | Domain users can RDP into CLIENT01 |
---
## 🎨 Fun Step – “Desktop Image added”
”** Before applying GPOs, users log in and put a image on a desktop ”**.
After policies apply, they can still see the file but **can’t set it as wallpaper**, showing how Group Policy overrides local control.
---
## 📸 Screenshots
| Image | Description |
|--------|-------------|
| <img width="1340" height="845" alt="resourcegroup-1" src="https://github.com/user-attachments/assets/b09402d8-67c5-4867-be81-bad1ae05780e" />| Resource Group created in Azure to contain all lab components |
| <img width="1413" height="852" alt="vnet-2" src="https://github.com/user-attachments/assets/6639fb61-b650-427b-83cb-35b1d1bc06fe" />| Virtual Network `vnet-adlab` created with custom subnet |
| <img width="1426" height="716" alt="nsg-3" src="https://github.com/user-attachments/assets/36f76a4d-e3c8-45c3-b837-552cc64a927a" />| NSG rule allowing RDP only from instructor’s public IP |
| <img width="1627" height="849" alt="vmserver-4" src="https://github.com/user-attachments/assets/e72dafc2-d83c-4305-97a0-51731578878d" />| Windows Server 2022 VM created (DC01) |
| <img width="1432" height="887" alt="vmclient-5" src="https://github.com/user-attachments/assets/703a729a-208c-41ee-85ce-36e8328c6b43" />| Windows 11 Pro client VM created and domain-joined |
| <img width="1911" height="1053" alt="ad-6" src="https://github.com/user-attachments/assets/6ba218b6-20e4-4430-bf95-e7fc2fc1078e" />| AD DS role installed and DC01 promoted to domain controller |
| <img width="571" height="146" alt="gpo-7" src="https://github.com/user-attachments/assets/ea1154da-3518-4835-a71c-558e6d0e1bf0" />| GPO preventing users from opening Control Panel |
| <img width="397" height="159" alt="gpo-8" src="https://github.com/user-attachments/assets/5696645b-610e-4888-9f66-f44e334c737f" />| GPO disabling Task Manager for domain users |
| <img width="1912" height="1074" alt="desktop-9" src="https://github.com/user-attachments/assets/644a90e0-039e-4960-9664-aae0f3504234" /> | User attempting to change wallpaper before GPO enforcement |
| <img width="762" height="526" alt="gpos-10" src="https://github.com/user-attachments/assets/757c0a26-238a-4e8e-98b4-8accf8ba38bd" />| Group Policy Management Console showing all enforced policies |
| <img width="1913" height="1079" alt="wallpapergpo-11" src="https://github.com/user-attachments/assets/3a823f62-99ac-4ede-a527-69d4fd9c23c6" />| Company logo wallpaper successfully applied through GPO |
| <img width="579" height="881" alt="rgdelete-12" src="https://github.com/user-attachments/assets/b52eafec-1cc1-4244-8ce4-c6f23cfa977e" />| Cleaning up all resources in Azure Resource Group to avoid charges |
---
## 🧩 Technical Highlights
- Secure RDP access limited to a single external IP
- Custom DNS (192.168.100.10) for internal name resolution
- Demonstrates Azure **Fabric DHCP** vs. traditional server DHCP
- Enforces domain policies with OU-scoped GPOs
- Uses shared UNC path (`\DC01\Wallpapers\logo.jpg`) for company wallpaper
---
## 💰 Estimated Cost
| Resource | Type | Cost/hr |
|-----------|------|---------|
| DC01 | B2s VM | ≈ $0.046 |
| CLIENT01 | B2s VM | ≈ $0.046 |
| **Total** | | **≈ $0.09/hr (~$0.27 for 3 hrs)** |
---
## 🏁 Results
✅ Domain environment successfully deployed
✅ CLIENT01 joined to domain `lab.local`
✅ GPOs applied and verified (`gpresult /h C:\GPOReport.html`)
✅ Wallpaper, Control Panel, and Task Manager restrictions enforced
✅ RDP access functioning for domain users
✅ All resources deleted post-lab to avoid costs
---
