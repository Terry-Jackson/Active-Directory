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
<br>
<br>
<br>
![clip 3 virtual machine](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/ce1984ea-fb35-4a1e-9c37-121821249a44)

Click on Virtual Machines and Create Azure Virtual Machine for Domain Controller.
<br>
<br>
<br>
![Clip 4 Setting the NIC to Static](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/e3aeefff-9eeb-4776-8b8d-98752a1b9573)
After (DC) is setup we will need to go into the NIC and change the IP address settings to Static.
<br>
<br>
<br>

 ![clip 2 Virtual Machine](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/82088a7c-cb34-49fd-aa84-7cc41babe748)
Next we will Create another (VM) setting up Client-1 with (Windows 10)
<br>
<br>
<br>
![Open Remote Desktop and Paste IP Address ](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/37a0eb72-a5cf-4f1a-8187-70a53c29c216)

Paste the public IP address of Client-1 in order to remote into computer.
<br>
<br>
<br>

![Add Credentials for Client 1 in order to remote into the system](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/b3c93987-5eed-49b0-93d0-a6ecb683d92b)

Add credentials for Client-1 in order to remote into (VM)
<br>
<br>
<br>

![Click yes in order to Remote Desktop into System](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/c3fa1d68-0ee6-4542-9868-77cd0adf8b14)

Click yes in order to proceed in remoting into system.
<br>
<br>
<br>

![Once I enable ICMPv4 On DC-1 the Request Timed out will Change ](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/32d06f3e-34e5-4b04-a685-a1475e0b5c64)

Logged into Client-1 and ping DC-1’s private IP address with ping -t <ip address> (perpetual ping) Once we go into the firewall settings of DC-1 and enable the ICMPv4 protocol the request timeout will change.
<br>
<br>
<br>

![Click on Inbound Rules 1](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/3e3e5670-e1de-4d94-b127-924c6f067599)

Find the Windows firewall settings and click on Inbound Rules. 
<br>
<br>
<br>

![Enable this Rule Private 2](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/cab41777-ae9c-4ccb-8305-75e33f0c3e9d)

Enable this Rule. 
<br>
<br>
<br>

![Enable this Rule Domain 3](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/9cf3bbca-e6ce-42e3-a70c-eb0dd46c83c4)

Enable this Rule as well for the ICMPv4 Protocol.
<br>
<br>
<br>

![No longer timing out](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/9c88415d-4cfc-465d-9e8c-fc6449cf6017)

Once I enable ICMPv4 On DC-1 the Request Timed out Changed.
<br>
<br>
<br>

![Installing Active Directory On Domain Controller 4](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/1bd2e2bc-77af-41fd-80cd-5e236abc3e88)

Click on Add Roles and Features. We are getting ready to install (AD DS)
<br>
<br>
<br>

![Start the Installation Wizard 5](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/41d8c4bf-e08d-4f40-afc4-2c82a98fb75c)

Click Next
<br>
<br>
<br>

![Click Next 6](https://github.com/Terry-Jackson/Active-Directory/assets/155121596/90126844-a6ef-41f8-804e-115e3e4e2f55)

Click Next
<br>
<br>
<br>







