# configure-ad
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Resources in Azure
- Ensure Connectivity between the windows 10 virtual machine and Domain Controller
- Create an Admin and Normal User Account in Active Directory
- Join windows 10 virtual machine to your domain

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/HfT8DEF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set up Recources by Creating the Domain Controller Virtual Machine (Windows Server 2022). Set Domain Controller’s NIC Private IP address to be static. Ensure that both VMs are in the same Vnet (you can check the topology with Network Watcher. Ensure Connectivity between the windows 10 virtual machine and Domain Controller.Login to windows 10 virtual machine with Remote Desktop and ping Domain's Controller private IP address with ping. Login to the Domain Controller and enable ICMPv4 in on the local windows Firewall.
</p>
<br />

<p>
<img src="https://i.imgur.com/ERMtqit.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”. Add new user to the “Domain Admins” Security Group
</p>
<br />

<p>
<img src="https://i.imgur.com/0e1jXDg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Join windows 10 virtual machine to your domain (mydomain.com)
From the Azure Portal, set virtual machine DNS settings to the Domain controller's Private IP address.

</p>
<br />
