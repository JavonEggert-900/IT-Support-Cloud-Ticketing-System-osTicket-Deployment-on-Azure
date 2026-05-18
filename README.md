# IT Support & Cloud Ticketing System — osTicket Deployment on Azure

<p align="center">
<img src="https://github.com/user-attachments/assets/523c00b3-1762-47b3-a05c-58e8b1774959" alt="VM Creation in Azure Portal" width="80%"/>
</p>

## Project Overview

This project demonstrates the full end-to-end deployment of osTicket — a widely used open source help desk ticketing system — on a Windows 10 Virtual Machine hosted in Microsoft Azure. Rather than simply using a ticketing system, this project builds one from the ground up: provisioning cloud infrastructure, configuring a web server, installing dependencies, setting up a database, and configuring the ticketing system as both an administrator and an end user. Every step mirrors what IT support professionals and cloud engineers encounter in real business environments.

# Environments and Technologies Used

* Microsoft Azure (Virtual Machines, Resource Groups, Remote Desktop Protocol)
* Windows 10 Pro (osticket-vm)
* Internet Information Services (IIS) with CGI
* osTicket v1.15.8
* PHP 7.3.8
* MySQL 5.5.62
* HeidiSQL
* PHP Manager for IIS
* URL Rewrite Module
* VC_redist (Visual C++ Redistributable)

# Operating Systems Used

* Windows 10 Pro (Azure Virtual Machine — osticket-vm)

# Project Objectives

* Deploy and configure a Windows 10 Virtual Machine in Microsoft Azure
* Install and configure IIS as a web server with CGI support
* Install and configure all osTicket dependencies including PHP, MySQL and HeidiSQL
* Deploy osTicket v1.15.8 and complete the full browser-based setup
* Configure roles, departments, teams, agents, users, SLA plans and help topics as an administrator
* Simulate the full ticket lifecycle from end user submission to agent resolution
* Perform post-installation security hardening and cloud resource cleanup

# High-Level Deployment and Configuration Steps

1. Deploy Windows 10 VM (osticket-vm) in Microsoft Azure and connect via RDP
2. Install and enable IIS in Windows with CGI support
3. Install all dependencies: PHP Manager, Rewrite Module, PHP 7.3.8, VC_redist, MySQL 5.5.62
4. Install osTicket v1.15.8 and configure IIS to serve the application
5. Enable required PHP extensions and rename configuration file
6. Create osTicket MySQL database using HeidiSQL
7. Complete browser-based osTicket setup and configure help desk branding
8. Configure roles, departments, teams, agents, users, SLA plans and help topics
9. Simulate full ticket lifecycle as end user and agent
10. Perform post-installation cleanup and delete Azure resources

# Deployment and Configuration Steps

## Step 1 — VM Creation in Azure Portal

<p align="center">
<img src="https://github.com/user-attachments/assets/523c00b3-1762-47b3-a05c-58e8b1774959" alt="VM Creation in Azure Portal" width="80%"/>
</p>

Deployed a Windows 10 Virtual Machine named osticket-vm in Microsoft Azure with 4 vCPUs in the Canada Central region. This is the cloud infrastructure foundation that hosts the entire osTicket help desk system — the same way businesses provision cloud servers to run their support platforms without managing physical hardware.

## Step 2 — RDP Connected into VM

<p align="center">
<img src="https://github.com/user-attachments/assets/065b148f-5226-4838-8b69-01493f179d4f" alt="RDP Connected into VM" width="80%"/>
</p>

Connected remotely into the osticket-vm using Remote Desktop Protocol. RDP is the standard method IT support teams and cloud administrators use daily to access and manage systems without physical access — a foundational skill for any help desk or cloud engineering role.

## Step 3 — IIS Enabled With CGI

<p align="center">
<img src="https://github.com/user-attachments/assets/8a39ccf1-051a-4c82-9c48-12743e6fd7a1" alt="IIS Enabled With CGI" width="80%"/>
</p>

Enabled Internet Information Services with CGI support under Application Development Features. IIS serves as the web server that hosts and delivers the osTicket application to users through a browser — the same foundational web server configuration used in enterprise application deployments across businesses of all sizes.

## Step 4 — osTicket Installation Files on Desktop

<p align="center">
<img src="https://github.com/user-attachments/assets/6aec9c17-a3cd-4f97-a7f1-41e95128116b" alt="osTicket Installation Files on Desktop" width="80%"/>
</p>

Downloaded and extracted the osTicket Installation Files folder to the desktop containing all required dependencies. Installed PHP Manager for IIS, the URL Rewrite Module, PHP 7.3.8, VC_redist and MySQL 5.5.62 — replicating the server-side dependency configuration required to run any PHP-based web application in a production business environment.

## Step 5 — osTicket Installer Loading

<p align="center">
<img src="https://github.com/user-attachments/assets/f016617e-f23a-44de-9cbd-13c9b1d5749a" alt="osTicket Installer Loading" width="80%"/>
</p>

Accessed the osTicket installer through IIS and observed that several PHP extensions were not enabled. Identified and enabled php_imap.dll, php_intl.dll and php_opcache.dll through PHP Manager — demonstrating the ability to diagnose and resolve application configuration issues before they impact end users or business operations.

## Step 6 — Successful Installation (Congratulations Page)

<p align="center">
<img src="https://github.com/user-attachments/assets/db071f44-e4c4-42fc-aa5a-19aca549e3d8" alt="Successful Installation Congratulations Page" width="80%"/>
</p>

Completed the full browser-based osTicket installation. The Congratulations screen confirmed successful deployment of a fully functional help desk ticketing system — the same outcome an IT team achieves when deploying a new support platform for their organization, ensuring business continuity and structured support operations.

## Step 7 — HeidiSQL Database Configuration

<p align="center">
<img src="https://github.com/user-attachments/assets/dd98d8d1-e05e-413e-9eb7-77486bf10c5f" alt="HeidiSQL Database Configuration" width="80%"/>
</p>

Used HeidiSQL to connect to the MySQL server and created the osTicket database. Database configuration is a critical backend skill for any IT professional managing web-based business applications — understanding where data lives and how it is structured underpins every ticketing system running in a production environment.

## Step 8 — osTicket Help Desk Login Page

<p align="center">
<img src="https://github.com/user-attachments/assets/987fc915-8d45-4559-be5e-f5caa139df4e" alt="osTicket Help Desk Login Page" width="80%"/>
</p>

Confirmed the help desk administrator login page was live and accessible. This is the portal that IT support agents use daily to log in, manage tickets, configure the system and support end users — the front door of every help desk operation in a business environment.

## Step 9 — Roles and Departments Configured

<p align="center">
<img src="https://github.com/user-attachments/assets/c52dd664-ee5c-45f1-8db0-7a774574b385" alt="Roles and Departments Configured" width="80%"/>
</p>

Configured the Supreme Admin role with full permissions and created the SysAdmins department. In a real business environment roles and departments control what agents can see and do — ensuring sensitive tickets are routed to the right team, access is appropriately restricted and the principle of least privilege is maintained across the support organization.

## Step 10 — SLA Plans Configured

<p align="center">
<img src="https://github.com/user-attachments/assets/dfd7a9cd-dd2c-4087-b8d9-27cfdd2c1158" alt="SLA Plans Configured" width="80%"/>
</p>

Configured three SLA plans reflecting real business urgency levels. Sev-A requires a 1 hour response with 24/7 coverage for critical outages. Sev-B requires a 4 hour response with 24/7 coverage for high priority issues. Sev-C requires an 8 hour response during business hours for standard requests. SLAs are how businesses hold IT teams accountable to response time commitments and are a foundational concept in every professional help desk environment.

## Step 11 — Agents and Users Created

<p align="center">
<img src="https://github.com/user-attachments/assets/99106758-9fd5-4970-8055-634914ec4358" alt="Agents and Users Created" width="80%"/>
</p>

Created agents Jane Doe in the SysAdmins department and John Doe in the Support department along with end user Karen. This mirrors the real world administrative task of onboarding new employees into an IT system and assigning them to appropriate teams — one of the most frequent responsibilities of a help desk administrator in any organization.

## Step 12 — Creating a Ticket as End User Karen

<p align="center">
<img src="https://github.com/user-attachments/assets/2d5e50fb-3a8e-4bac-9d04-759ce4ce18e6" alt="Creating a Ticket as End User" width="80%"/>
</p>

Submitted a ticket from the end user perspective as Karen reporting that the entire mobile and online banking system was down. Simulating the user experience is critical for help desk professionals — understanding how tickets are submitted and what information users provide helps agents triage and respond more effectively to business-critical issues.

## Step 13 — Ticket Properties Viewed as Agent John

<p align="center">
<img src="https://github.com/user-attachments/assets/174d0463-d56f-4c69-8291-cecd68ba3c92" alt="Ticket Properties as Agent" width="80%"/>
</p>

Logged in as agent John and reviewed the incoming ticket in its unassigned state with default SLA applied. This represents the real world first touch of a ticket — an agent opens the queue, reviews what came in and begins the triage process that determines how the business responds to the reported issue.

## Step 14 — Setting Ticket Properties

<p align="center">
<img src="https://github.com/user-attachments/assets/cd798bbf-b18d-48ac-ab3e-89d1eb376712" alt="Setting Ticket Properties" width="80%"/>
</p>

Updated the ticket priority to Emergency, escalated the SLA to Sev-A requiring a 1 hour response and assigned the ticket to the appropriate agent. This reflects the real world triage process that determines how quickly and by whom a business-critical issue gets resolved — a banking system outage affects thousands of customers and every minute of downtime has direct business impact.

## Step 15 — Resolving and Closing a Ticket

<p align="center">
<img src="https://github.com/user-attachments/assets/f4922f80-3c9e-413d-830b-e7f435c2ac75" alt="Resolving and Closing a Ticket" width="80%"/>
</p>

Resolved the ticket as agent Jane Doe and closed it with a resolution note. This completes the full ticket lifecycle from end user submission to triage to escalation to resolution — demonstrating end-to-end familiarity with how IT support workflows operate and how businesses track the resolution of issues that impact their operations and customers.

## Step 16 — Setup Folder Deleted

<p align="center">
<img src="https://github.com/user-attachments/assets/c06e23ec-cf32-4435-85f7-caedce3f8091" alt="Setup Folder Deleted" width="80%"/>
</p>

Deleted the setup folder at C:\inetpub\wwwroot\osTicket\setup after installation completion. Leaving the setup folder accessible after deployment is a known security vulnerability — any user who discovers the URL could potentially reconfigure or compromise the system. Removing it immediately after installation is a standard security hardening practice in production environments.

## Step 17 — ost-config.php Set to Read Only

<p align="center">
<img src="https://github.com/user-attachments/assets/76d47a5a-8794-4bd2-b3b9-9d563a7f613a" alt="ost-config.php Set to Read Only" width="80%"/>
</p>

Set ost-config.php permissions to Read Only under Everyone — preventing unauthorized modification of the system configuration file after deployment. This post-installation security hardening step protects the business from configuration tampering and reflects the security-conscious mindset required of IT professionals managing production systems.

## Step 18 — Azure Resource Group Deletion Confirmed

<p align="center">
<img src="https://github.com/user-attachments/assets/4e53fb2b-efff-43bb-9d64-bf34e4ed0a93" alt="Azure Resource Group Deletion Confirmed" width="80%"/>
</p>

Deleted the Azure Resource Group and all associated resources after lab completion. Proper cloud resource cleanup is a real and valued skill — unmanaged cloud resources cost businesses thousands in unnecessary charges monthly. Consistently practicing this discipline reflects the cost-conscious approach required of cloud administrators and engineers managing business infrastructure.

# Key Skills Demonstrated

* Microsoft Azure — Virtual Machine deployment and cloud resource management
* Remote Desktop Protocol — remote VM access and administration
* IIS Web Server — installation, configuration and application hosting
* PHP Configuration — dependency installation and extension management
* MySQL Database Administration — database creation and connection via HeidiSQL
* osTicket Administration — roles, departments, SLA plans, agents, users and help topics
* IT Ticketing Workflow — full ticket lifecycle from submission to resolution
* Security Hardening — post-installation permission configuration and cleanup
* Technical Troubleshooting — diagnosed and resolved a real 404 error during deployment
* Cloud Cost Management — proper resource deletion after lab completion

# Business Applications

Every component of this project maps directly to how businesses operate their IT support infrastructure. Ticketing systems like osTicket are the backbone of IT departments — they track every user issue, enforce response time commitments through SLAs, route tickets to the right teams through departments and roles, and provide management with visibility into support performance. By deploying this system from scratch rather than simply using it, this project demonstrates an understanding of not just how to work within a ticketing system but how to build, configure and maintain one. For any business deploying a new support platform, migrating from one system to another, or onboarding new IT staff, these skills represent real operational value. The cloud deployment on Azure further demonstrates the ability to provision and manage business applications in modern cloud infrastructure — a critical capability as organizations continue moving away from on-premise systems.

# Lessons Learned

The most valuable moment in this project was not planned. During installation, the osTicket site returned a 404 error when accessed through the browser. Instead of starting over, the issue was systematically diagnosed — tracing it back to the upload folder inside wwwroot not having been renamed to osTicket as required. Renaming the folder resolved the error immediately and the site loaded successfully. This experience reinforced a fundamental truth in IT support and cloud engineering: real troubleshooting is not about memorizing steps, it is about methodically identifying where a process broke down and applying logical reasoning to fix it. That is a skill no lab checklist can teach — it only comes from actually encountering the problem and working through it.
