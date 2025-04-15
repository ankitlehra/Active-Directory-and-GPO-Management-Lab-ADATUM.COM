# Enterprise Active Directory and GPO Management Lab – ADATUM.COM

This lab demonstrates a full Active Directory and Group Policy Management implementation in a simulated enterprise setup using Windows Server 2022. The goal was to configure user accounts, organizational units, delegation, permissions, GPOs, and firewall rules in a domain environment.

---

## 🛠️ Tools Used

- Active Directory Users and Computers (ADUC)
- Active Directory Administrative Center (ADAC)
- Group Policy Management Console (GPMC)
- Windows Admin Center
- Windows Defender Firewall with Advanced Security
- Event Viewer

---

## 📋 Key Tasks & Activities

### 1. **Active Directory Management**
- Created a domain structure for `adatum.com`.
- Built OUs like IT, Marketing, Managers, Service Accounts, Research, etc.
- Created and managed user accounts (e.g., Colin Hunt, Beth Burke).
- Applied logon hour restrictions and account policies.
- Enabled protection against accidental deletion.

### 2. **Group and Role Management**
- Created Security Groups like `ITADMINS`.
- Assigned users to groups.
- Delegated specific control to ITADMINS (reset passwords, manage group memberships).

### 3. **Group Policy Management**
- Created and linked GPO `EndpointBaseline-6803` to domain and Domain Controllers.
- Configured ADMX templates including:
  - LAPS (Local Administrator Password Solution)
  - MSS security settings
  - Start Menu, Control Panel, and Windows Components

### 4. **Firewall Hardening**
- Configured inbound and outbound firewall rules:
  - Allowed: Notepad, RDP, system apps.
  - Blocked: Internet Explorer, Edge, SMTP, Xbox services.
- Verified logs in Event Viewer (RuleName: Block Internet Explorer).

---

## 📸 Screenshots

All configuration and setup steps are documented in the `/images` folder. Key highlights:
- ADUC configuration
- Group creation and delegation
- GPO linking and editing
- Firewall rules and log validation
