# Windows Server Active Directory Home Lab

## Overview

This project documents the setup of a Windows Server 2022 Active Directory home lab using VMware. The lab simulates a small business domain environment with a domain controller, Windows client machine, user accounts, group permissions, DNS, DHCP, Group Policy, and troubleshooting scenarios.

The goal of this project is to demonstrate hands on IT support skills, including user account management, domain authentication, basic network services, endpoint configuration, and structured troubleshooting.

## Lab Objectives

- Build and configure a Windows Server domain environment with Active Directory Domain Services.
- Join Windows 10/11 client machines to the domain.
- Create and manage user accounts, groups, password resets, and account permissions.
- Configure and test DNS and DHCP services.
- Apply Group Policy Objects to enforce user and system restrictions.
- Troubleshoot login failures, DNS issues, and network connectivity problems.
- Document each step with screenshots for portfolio proof.


---

## Lab Environment

| Device   | OS                    | Purpose                          |
|----------|----------------------|----------------------------------|
| DC01     | Windows Server 2022  | Domain Controller (AD, DNS, DHCP) |
| CLIENT01 | Windows 10/11        | Domain Client Machine             |

---

## Network Configuration

| Device   | IP Address      | DNS Server      |
|----------|----------------|-----------------|
| DC01     | 192.168.1.10   | 192.168.1.10    |
| CLIENT01 | DHCP Assigned  | 192.168.1.10    |

---

## Step 1: Virtual Machine Setup

I created two virtual machines in VMware to simulate a small business environment. DC01 acts as the domain controller and CLIENT01 acts as a user workstation.

![VM Setup](screenshots/01-vm-setup.png)

---

## Step 2: Static IP Configuration

I configured a static IP address on DC01 to ensure reliable communication for domain services and DNS.

![Static IP](screenshots/02-dc01-static-ip.png)

---

## Step 3: Installing Active Directory Domain Services

I installed the Active Directory Domain Services role to enable domain management functionality.

![AD DS Installed](screenshots/03-ad-ds-installed.png)

---

## Step 4: Domain Controller Setup

I promoted the server to a domain controller and created the domain homelab.local.

![Domain Setup](screenshots/04-domain-controller-promotion.png)

---

## Step 5: Organizational Units

I created Organizational Units to organize users, groups, and systems within the domain.

![OUs](screenshots/06-organizational-units.png)

---

## Step 6: User and Group Management

I created domain users and groups and assigned group memberships to simulate access control.

![Users](screenshots/07-domain-users-created.png)

![Groups](screenshots/08-domain-groups-created.png)

---

## Step 7: Password Policy

I configured password and account policies using Group Policy to enforce security requirements.

![Password Policy](screenshots/10-password-policy.png)

---

## Step 8: DNS Configuration

I verified DNS configuration and tested name resolution using command-line tools.

![DNS](screenshots/12-dns-zone.png)

---

## Step 9: DHCP Configuration

I configured DHCP to automatically assign IP addresses to client machines.

![DHCP](screenshots/15-dhcp-scope.png)

---

## Step 10: Domain Join

I joined CLIENT01 to the domain and verified successful connection to the domain controller.

![Client Joined](screenshots/18-client-joined-domain.png)

---

## Step 11: Domain Login

I logged into the client machine using a domain account and verified authentication.

![Login](screenshots/19-domain-user-login.png)

---

## Step 12: Group Policy

I created and applied a Group Policy Object to enforce user restrictions and verified it on the client machine.

![GPO](screenshots/21-gpo-created.png)

---

## Troubleshooting Scenarios

### Login Failure

Problem: User could not log in  
Cause: Account disabled  
Fix: Re-enabled account in Active Directory  

---

### DNS Issue

Problem: Domain not resolving  
Cause: Incorrect DNS settings  
Fix: Updated DNS to domain controller  

---

### Network Issue

Problem: No connectivity  
Cause: Network adapter disabled  
Fix: Re-enabled adapter and renewed IP  

---

## Troubleshooting Method

For each issue, I followed a structured troubleshooting process:

1. Identify the issue  
2. Gather information  
3. Test possible causes  
4. Apply a fix  
5. Verify resolution  
6. Document results  

---

## Skills Demonstrated

- Active Directory administration  
- Windows Server configuration  
- User account management  
- DNS and DHCP configuration  
- Group Policy management  
- Domain authentication  
- IT troubleshooting  
- Technical documentation  
