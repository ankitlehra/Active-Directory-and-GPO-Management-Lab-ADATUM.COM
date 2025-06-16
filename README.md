# Enterprise Active Directory and GPO Management Lab – ADATUM.COM

This lab demonstrates a full Active Directory and Group Policy Management implementation in a simulated enterprise setup using Windows Server 2022. The goal was to configure user accounts, organizational units, delegation, permissions, GPOs, and firewall rules in a domain environment.

---

## Tools Used

- Active Directory Users and Computers (ADUC)
- Active Directory Administrative Center (ADAC)
- Group Policy Management Console (GPMC)
- Windows Admin Center
- Windows Defender Firewall with Advanced Security
- Event Viewer

---

## Key Tasks & Activities

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

### OU and Account Setup
![Service Account OU](images/01-OU-Service-Account.png)
*Organizational Unit created for Service Accounts.*

![VIP User Properties](images/02-VIP-Account-Properties.png)
*User properties of a VIP user – Colin Hunt.*

![Logon Hours](images/03-Logon-Hours-Colin.png)
*Logon hours configured for weekdays, 9 AM to 6 PM.*

![Object Protection](images/04-Object-Details-prevent-accidental-deletion-Colin.png)
*User object protected from accidental deletion.*

### User Groups and Admin Center
![IT OU Users](images/05-OU-IT-Users.png)
*IT OU with 4 users*

![ADAC Overview](images/06-ADAC-Overview.png)
*Active Directory Administrative Center Overview*

![Server Manager](images/07-Server-Manager-View.png)
*Web Server Manager Active Directory view*

### Group Management & Delegation
![ITADMINS Group Members](images/08-Group-Members-ITADMINS.png)
*ITADMINS group with 4 members*

![Delegation Wizard](images/09-Delegation-Complete.png)
*Delegation of Control Wizard complete screen*

### OU Permissions & Security
![Advanced Permissions](images/10-Advanced-Permissions-Research.png)
*Advanced Permissions - Research OU – advanced security settings*

### GPO Configuration
![GPO Scope – EndpointBaseline](images/11-GPO-EndpointBaseline-Scope.png)
*Shows the EndpointBaseline-6803 GPO and its linked scope.*

### Firewall Configuration
![Firewall Rules – Inbound & Outbound](images/12-WindowsFirewall-Inbound-Outbound-Rules.png)
*Firewall Rules – Inbound & Outbound (notepad allowed, IE blocked).*

![Firewall Log – Event Viewer](images/13-WindowsFirewall-EventLog.png)
*Firewall Log – Event Viewer(Shows a log entry for the “Block Internet Explorer” firewall rule.)*

### GPO ADMX Templates
![ADMX Settings](images/15-GPO-Editor-ADMX-Templates.png)
*ADMX Settings(GPO editor with ADMX templates from central store (Control Panel, LAPS, etc.))*
