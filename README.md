<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b>

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>
Welcome to my first in-depth IT tutorial! To begin we will have to create a Virtual machine using the Microsoft Azure portal(portal.azure.com). We will be using a VM(virtual machine) which is a remote computer. We are using a VM in order to protect our physical machine just in case something malfunctions, and also have a clean slate computer to continually replicate the lab on. Create a resource group and title it "osTicket". Afterwards create a VM with 2-4 CPUs. In this example I will be using 4 CPUs.
<p>
<p>
<img width="1720" height="839" alt="slide1" src="https://github.com/user-attachments/assets/c5d22a3c-7654-43ef-8192-09ba521d9aff" />

</p>
<p>
Next simply connect to your newly created VM using RDP using the public IPv4 address. If you are a Mac user you will have to download Microsoft Remote Desktop(RDP).
</p>
<br />
<p>
<p>
<img width="1255" height="782" alt="slide2" src="https://github.com/user-attachments/assets/662505fb-a690-4596-a040-70681f160df5" />
</p>
<p>
Alright, now that you are connected to your VM you will have to enable IIS. Simply access the control panel then select uninstall a program. Off to the left select "Turn windows features on or off". A list will appear then you will enable Internet Information Services.
</p>
<br />

<p>
<img width="1209" height="638" alt="slide3" src="https://github.com/user-attachments/assets/0cf5a6a4-2f22-45fa-8875-ac138c4130ce" />

</p>
<p>
Excellent. Now that you have enabled IIS we need to install Web Platform Installer. I have provided a link here: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 That link will provide you with all of the material you need to download to get osTicket up and running. Simply click the link and install the Web Platform Installer.
</p>
<br />
<img width="1039" height="817" alt="slide4" src="https://github.com/user-attachments/assets/c8c75368-12a1-4a2f-aaae-19b792671013" />
</p>
<br />

<p>
Once you have installed Web Installer Platform open it. From inside the application you are going to install MySQL 5.5 Afterwards install x86 version of PHP up until 7.3. There are some failed files such as C++ redistributable package as well as PHP 7.3.8 and PHP Manager for IIS those files can be found with the install link.


