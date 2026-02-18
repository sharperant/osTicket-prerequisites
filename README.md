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

- Creating a Virtual Machine in Azure
- Installing osTicket v1.15.8
- Installing HeidiSQL
- Installing MySQL then and set up user and pass
- Installing PHP
- Installing Microsoft Visual C++ Redistributable

<h2>Installation Steps</h2>
Hello and welcome to my in-depth IT tutorial! To begin we will have to create a Virtual machine using the Microsoft Azure portal(portal.azure.com). First create a Resource Group inside Azure. Now, create a Windows 10 Virtual Machine (VM),When creating the Virtual Machine, make sure your VM and resource group have the same region. It is advisable to remember the Username and password you chose and allow Azure to create a new Virtual Network (Vnet). After clicking on the 'Review and create" button,it might take a while to complete deployment.
<p>
<p>
<img width="2143" height="1210" alt="slide1" src="https://github.com/user-attachments/assets/4051abd1-be32-4a6c-88bc-d829619e6164" />
</p>
<p>
<img width="1455" height="291" alt="slide2" src="https://github.com/user-attachments/assets/d5c64688-869b-4698-90a5-0c8467c2479c" />
</p>
<br />
<p>
<p>
Open Windows Remote Desktop on your computer and paste the public IP address of the virtual machine that was created, then click on the "connect" button. You will then be asked for the Username and Password of the VM, do that to access the VM.
<p>
<p>
<img width="1285" height="647" alt="slide3" src="https://github.com/user-attachments/assets/b44709a8-2132-4137-b35b-0438725bb95e" />
<p>
<p>
Within the Virtual machine, download the osTicket-Installation-Files.zip.
<p>
<p>
<img width="1512" height="522" alt="slide4" src="https://github.com/user-attachments/assets/a018580e-2f02-48b3-b58a-eec89d6840c0" />
<p>
<p>
Unzip it onto your desktop by right clicking it and click on "Extrack all".
<p>
<p>
<img width="585" height="812" alt="slide5" src="https://github.com/user-attachments/assets/e177c4aa-ada3-4871-a489-2cbb08702d93" />
<p>
<p>



