# Active Directory User & Access Management Lab

## Overview

A hands-on Windows domain lab built in VirtualBox to practice Active Directory, Group Policy, account lockout, and least-privilege file-share access.

## Architecture

The diagram summarizes the lab environment, domain controller and client, identity and policy management, and HR/Finance share access controls.

![Active Directory lab architecture](active-directory-user-access-architecture.png)

## Lab Environment

- VirtualBox virtual machines
- Windows Server 2022 domain controller
- Windows 10 domain client
- Active Directory domain: `lab.local`

## Tasks and Evidence

### 1. Prepare the server and client VMs
Prepared the Windows Server environment and configured the Windows client VM in VirtualBox.

![Server roles and setup](screenshots/01-server-roles.png)
![Windows client VM configuration](screenshots/02-virtualbox-client-vm.png)
![Windows client installation](screenshots/03-windows-client-install.png)

### 2. Verify networking and join the domain
Checked client network connectivity, then configured the client to join the `lab.local` domain.

![Network connectivity test](screenshots/04-network-connectivity-test.png)
![Domain join configuration](screenshots/05-domain-join.png)

### 3. Verify domain computer and organize directory objects
Used Active Directory Users and Computers to verify the domain client and create organizational units for lab administration.

![Domain computer in Active Directory](screenshots/06-domain-computers-console.png)
![Create an organizational unit](screenshots/07-create-organizational-unit.png)
![Organizational units, users and groups](screenshots/08-organizational-units-users-groups.png)

### 4. Configure Group Policy and test account lockout
Configured password and account lockout policy settings, refreshed policy, and tested the lockout behavior.

![Password policy configuration](screenshots/09-password-policy.png)
![Account lockout policy configuration](screenshots/10-account-lockout-policy.png)
![Group Policy update](screenshots/11-policy-update-verification.png)
![Account lockout test](screenshots/12-account-lockout-test.png)

### 5. Review user settings and security audit events
Inspected domain user settings and reviewed Windows security events associated with account activity and lockout.

![Domain user settings](screenshots/13-domain-user-settings.png)
![Account lockout event](screenshots/14-account-lockout-event.png)
![Security audit event](screenshots/15-security-audit-event.png)

### 6. Configure least-privilege file-share permissions
Applied and reviewed NTFS permissions for the HR and Finance shares. The lab evidence shows HR share permissions and a denied attempt to access Finance as intended.

![Inherited permissions prompt](screenshots/16-inherited-permissions.png)
![Select a security group](screenshots/17-select-security-group.png)
![HR share NTFS permissions](screenshots/18-hr-share-ntfs-permissions.png)
![File shares](screenshots/19-file-shares.png)
![Finance access denied test](screenshots/20-finance-access-denied.png)

## Outcome

The lab demonstrates domain setup, directory organization, Group Policy-based security controls, account lockout testing, Windows security event review, and share permissions aligned with least privilege.

## Scope

Completed in an isolated VirtualBox lab for learning and defensive administration practice.
