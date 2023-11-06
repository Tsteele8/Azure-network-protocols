<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://youtu.be/wuIE4p4io7Q?si=nu5eDYIu_OkZc-E7)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create VMs 
- Allow Permissions on DC-1's Firewall
- Test Communication between VMs
- Setup Remote Desktop for Non-Admin Users on Client-1
- Create Additional Users via Powershell ISE
- Test New User Accounts

<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/Tsteele8/Azure-network-protocols/assets/149441408/5551fa1e-c38b-4096-a06c-9fee865744a1)


<p>
Log into Azure --> search "virtual machines" --> click "create azure virtual machine" to create VM#1. Name this first virtual machine "DC-1" using your current region --> set the image type as "Windows Server 2022"
</p>
<br />

![image](https://github.com/Tsteele8/Azure-network-protocols/assets/149441408/177783e1-061a-4b60-9118-b1a24cbd7976)


<p>
Remote Desktop into DC-1 via windows firewall security settings --> Advanced settings --> inbound/outbound rules to allow "IPV4 permissions" on DC-1's Firewall. This will open the firewall for connectivity after DC-1 is converted into a domain.


</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
