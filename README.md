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

- Setup a VM Domain Controller (Windows Server2022) as well a Client VM (Windows 10) 
- Remote Desktop into Domain Controller from Client 1 with (perpetual Ping)
- Install Active Directory Domain Services onto DC
- Setup a New Forest
- Create Organizational Units in (ADUC)
- Run Script in Powershell_ise as administrator to populate user accounts
<h2>Deployment and Configuration Steps</h2>

![image](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/f30e33e2-734f-4f56-a4e8-f68d002deaeb)
Create a resource group. Once you have the resource group created. The next step will be to create a (VM) for your Domain Controller using (Windows Server 2022)


![clip 3 virtual machine](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/ce1984ea-fb35-4a1e-9c37-121821249a44)

Click on Virtual Machines and Create Azure Virtual Machine for Domain Controller.

![Clip 4 Setting the NIC to Static](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/e3aeefff-9eeb-4776-8b8d-98752a1b9573)
After (DC) is setup we will need to go into the NIC and change the IP address settings to Static.

![clip 2 Virtual Machine](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/82088a7c-cb34-49fd-aa84-7cc41babe748)
Next we will Create another (VM) setting up Client-1 with (Windows 10)









