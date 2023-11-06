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

![image](https://github.com/Tsteele8/Azure-network-protocols/assets/149441408/9a6254fe-8178-4cb7-bbba-c7240b656841)


<p>
Ensure communication between both VMs via perpetual ping using cmd:ping -t (Ip Address).
</p>
<br />

![image](https://github.com/Tsteele8/Azure-network-protocols/assets/149441408/8739aa3e-474f-450e-bbc7-66a1cf38d828)

Use Remote Desktop in the system settings to allow domain users access for all non-admin users on Client-1 VM under "user accounts" --> "select users that can remotely access this PC" --> click "add" and type in "domain users".

![image](https://github.com/Tsteele8/Azure-network-protocols/assets/149441408/e69d177e-c06b-45a2-afa9-e5260ed08552)

Use a random account generating script to create at least 100 users for this lab. Upload script via "Powershell ISE" (run as administrator) to Client-1. This will create 100 new users with random names. This is done to simulate employees within the company.

![image](https://github.com/Tsteele8/Azure-network-protocols/assets/149441408/26673b40-12d8-40ba-9e15-626425e4bcb1)

Log into any newly generated user account on Client-1 VM. The login attempt with the user's name & generic password should be successful. That is the conclusion of this lab.



