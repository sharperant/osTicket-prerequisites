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
<img width="1080" height="527" alt="slide1modify1" src="https://github.com/user-attachments/assets/d4d29e5a-0ed6-4b55-b8ee-5b76910b5ba6" />
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
</p>
<br />
<p>
<p>
<img width="1071" height="716" alt="slide5" src="https://github.com/user-attachments/assets/8509a9f1-c660-4147-a269-37c5afeb1646" />
</p>
<br />
<p>
<p>
Next download osTicket. Then extract and copy the "upload" folder into c:\inetpub\wwwroot. Afterwards rename the folder to osTicket
</p>
<br />
<p>
<p>
<img width="1012" height="547" alt="slide6" src="https://github.com/user-attachments/assets/7d0250b5-19d5-4240-96ab-60ef112695a3" />
</p>
<br />
<p>
<p>
Open IIS Manager and restart the server. Once inside IIS manager go to Sites->Default->osTicket on the right, click "Browse*.80" from there your default browser should open osTicket webserver.
</p>
<br />
<p>
<p>
<img width="1047" height="554" alt="slide7" src="https://github.com/user-attachments/assets/4f274aac-8566-4f30-9c96-0137f37aba5b" />
</p>
<br />
<p>
<p>
Go back into IIS manager and enable some extensions. To do this you have to go to Sites->Default->osTicket Then double click on PHP manager. Click on "Disable or enable an extension" Enable "php_intl.dll" & "php_opcache.dll" then refresh the osTicket webserver and obsereve the changes "Intl Extension" should now be enabled.
</p>
<br />
<p>
<p>
<img width="1289" height="684" alt="slide8" src="https://github.com/user-attachments/assets/e4c697f9-3848-45b4-a8d7-3799720cb42b" />
</p>
<br />
<p>
<p>
Go back into c:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php rename the file to c:\inetpub\wwwroot\osTicket\include\ost-config.php Assign permissions to ost-config.php Disable inheritance->Removeall New Permissions->Everyone->all
</p>
<br />
<p>
<p>
<img width="1292" height="622" alt="slide9" src="https://github.com/user-attachments/assets/f7128cac-d6b7-41df-99e4-6426ece7451a" />
</p>
<br />
<p>
<p>
Afterwards continue setting up osTicket in the browser (click continue) then you will name the Helpdesk to your liking. Select a default email that will receive emails from customers who submit tickets.
</p>
<br />
<p>
<p>
<img width="862" height="810" alt="slide10" src="https://github.com/user-attachments/assets/cf591e1c-d1e0-4727-977c-b4ed198f1cca" />
</p>
<br />
<p>
<p>
Continue Setting up osticket in the browser MySQL Database: osTicket MySQL Username: root MySQL Password: Password1 Click “Install Now!” Congratulations, hopefully it is installed with no errors! Clean up Delete: C:\inetpub\wwwroot\osTicket\setup Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
