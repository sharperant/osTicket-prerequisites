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
<h4 align="left" tabindex="-5" class="heading-element" dir="auto"> Hello and welcome to my in-depth IT tutorial! To begin we will have to create a Virtual Machine using the Microsoft Azure portal (portal.azure.com). First create a Resource Group inside Azure. Now, create a Windows 10 Virtual Machine (VM). When creating the Virtual Machine, make sure your VM and Resource Group have the same region. It is advisable to remember the Username and password you chose and allow Azure to create a new Virtual Network (VNet). After clicking on the "Review and create" button, it might take a while to complete deployment.</h4>
<p>
<p>
<img width="80%" height="1210" alt="slide1" src="https://github.com/user-attachments/assets/4051abd1-be32-4a6c-88bc-d829619e6164" />
</p>
<p>
<br />
<p>
<p>
<img width="80%" height="291" alt="slide2" src="https://github.com/user-attachments/assets/d5c64688-869b-4698-90a5-0c8467c2479c" />
</p>
<br />
<p>
<p>
Open Windows Remote Desktop on your computer and paste the public IP address of the virtual machine that was created, then click on the "connect" button. You will then be asked for the Username and Password of the VM, do that to access the VM.
<p>
<p>
<img width="80%" height="647" alt="slide3" src="https://github.com/user-attachments/assets/b44709a8-2132-4137-b35b-0438725bb95e" />
<p>
<p>
Within the Virtual machine, download the osTicket-Installation-Files.zip.
<p>
<p>
<img width="80%" height="522" alt="slide4" src="https://github.com/user-attachments/assets/a018580e-2f02-48b3-b58a-eec89d6840c0" />
<p>
<p>
Unzip it onto your desktop by right clicking it and click on "Extract All".
<p>
<p>
<img width="80%" height="812" alt="slide5" src="https://github.com/user-attachments/assets/e177c4aa-ada3-4871-a489-2cbb08702d93" />
<p>
<p>
Now we have to enable IIS in Windows (It's a web server that will help run ostickets). Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Look for "Internet Information Services".
<p>
<p>
<img width="80%" height="1238" alt="slide6" src="https://github.com/user-attachments/assets/9a3dc423-f32d-430f-93f3-e1496a8232ad" />
<p>
<p>
Expand IIS > Expand the "World Wide Web" > Expand "Application Developer" > Check the "CGI" button & press "Ok". You will need CGI to download the PHP Manager which is a back-end web programming language that allows osTicket to run off a web browser.
<p>
<p>
<img width="80%" height="929" alt="slide7" src="https://github.com/user-attachments/assets/6f373a08-00a3-4ef9-a74a-2a92a6fd2bd1" />
<p>
<p>
Installing PHP Manager

Now we need to download PHP which is a backend web server language that is needed to run osTicket.
Go to osticket installation folder > Double click "PHPManagerforIIS" > Agree with all the terms and we've now downloaded the PHP manager.
<p>
<p>
<img width="80%" height="495" alt="slide8" src="https://github.com/user-attachments/assets/5ebcbeba-98fb-4d8b-909e-693e8db6584e" />
<p>
<p>
<img width="80%" height="837" alt="slide9" src="https://github.com/user-attachments/assets/21110981-b168-4b07-afd6-f7fb00257668" />
<p>
<p>
Installing Rewrite Module

Go to osticket installation folder > Double click "rewrite_amd64" > Agree with all the terms and it should now be installed onto the Computer.
<p>
<p>
<img width="80%" height="960" alt="slide10" src="https://github.com/user-attachments/assets/c3e7e56e-6980-41ce-9548-a39b0b6850b0" />
<p>
<p>
CREATE DIRECTORY C:\PHP

Go to File Explorer > Click on "This PC" > Click on "Windows C(drive)" and create a new folder named "PHP". Now go to the OSticketinstallation-folder > Right click on "php-7.3.8-nts-Win32-VC15-x86" to extract all > click "Browse" and go to the C drive and direct the extraction to the PHP folder.
<p>
<p>
<img width="80%" height="544" alt="slide11" src="https://github.com/user-attachments/assets/a5278d17-f6c6-484a-86ee-8b50f6089c18" />
<p>
<p>
DOWNLOADING VC_REDIST
Double click on "VC_redist.x86, Agree with it's terms and agreements and finish installing.
<p>
<p>
<img width="80%" height="791" alt="slide12" src="https://github.com/user-attachments/assets/3c815c20-5f18-4967-aee7-8f28e9af35e7" />
<p>
<p>
DOWNLOAD MySQL
Go to “osTicket-Installation-Files” folder > Doubleclick "mysql-5.5.62-win32" to begin installation, Make sure to choose "Typical setup". Lauch it after install and insert the username and password of your choice then make sure to tick all the box.
<p>
<p>
<img width="80%" height="798" alt="slide13" src="https://github.com/user-attachments/assets/5cd6c69b-596c-4372-a610-ed976153b561" />
<p>
<p>
<br />
<p>
<p>
<img width="80%" height="1366" alt="slide14" src="https://github.com/user-attachments/assets/46a0bbed-12ea-4407-a6af-7b2da3e3f2a1" />
<p>
<p>
<br />
<p>
<p>
Next, search for IIS in the searchbar and open it as an admin > Double click "PHP Manager" > Click "Register new PHP version" > Browse to the PHP floder and choose "php-cgi" > Now reload IIS by clicking Stop(wait) and start.
<p>
<p>
<img width="80%" height="1550" alt="slide15" src="https://github.com/user-attachments/assets/4ca5c2c4-44a5-49d2-b82d-1c15c4f801ae" />
<p>
<p>
<img width="80%" height="584" alt="slide16" src="https://github.com/user-attachments/assets/676fb306-ca26-411b-8fea-b67eef484b4c" />
<p>
<p>
Installing osTicket v1.15.8
Extract and copy the “upload” folder into the C drive "wwwroot" (“c:\inetpub\wwwroot”). Then change the file named from "upload" to "osTicket"
<p>
<p>
<img width="80%" height="421" alt="slide17" src="https://github.com/user-attachments/assets/44875a95-6d01-42f4-a4ff-b77e5d47f89a" />
<p>
<p>
<img width="80%" height="427" alt="slide18" src="https://github.com/user-attachments/assets/37b4dcad-761c-48a3-8f2e-fda9ca2b17cb" />
<p>
<p>
Enable some Extensions in IIS
Under IIS manager, go to sites--> defualt-->ostickets in the top left hand corner > Click osticket > Click "browse 80" under manage folder to open the osticket web page. Now back to IIS, Double-click PHP Manager > Click “Enable or disable an extension” > Click enable "php_imap.dll" "php_intl.dll" and "php_opcache.dll".
<p>
<p>
<img width="80%" height="1591" alt="slide19" src="https://github.com/user-attachments/assets/56693907-2e8d-41dc-b124-89dda3b3c49a" />
<p>
<p>
<img width="80%" height="709" alt="slide20" src="https://github.com/user-attachments/assets/7faa5ceb-63cc-475f-ac92-179e3bd4de57" />
<p>
<p>
Now refresh the osTicket site in your browser to observe the changes.
<p>
<p>
<img width="80%" height="1562" alt="slide21" src="https://github.com/user-attachments/assets/bbafb3fc-953e-4a94-8f21-97d527102afe" />
<p>
<p>
Rename
Go to Windows C drive > Click "inetpub" > Click "wwwroot" > Click "osticket" > Click "include" and then you change the name of the php from "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to "C:\inetpub\wwwroot\osTicket\include\ost-config.php"
<p>
<p>
<br />
<p>
<p>
Assign Permissions (ost-config.php)
To assign Permissions, Right click "ost-config.php" > Click "Properties" > Click "Advanced" > Disable inheritance >Click "remove all inherited permissions from the object" > Add everyone to the permissions.
<p>
<p>
<img width="80%" height="753" alt="slide22" src="https://github.com/user-attachments/assets/40eada7a-1dbe-4c60-8ec1-e970640a5851" />
<p>
<p>
Continue Setting up osTicket
Open osTicket in the browser or refresh the webpage and input all the information required. Make sure the email you choose is your work email which you will use to receive email from customers.
<p>
<p>
<img width="80%" height="1519" alt="slide23" src="https://github.com/user-attachments/assets/99a5341b-c24a-41a9-8840-8839c5759151" />
<p>
<p>
Downloading and Installing HeidiSQL
Go back to the “osTicket-Installation-Files” folder and Double click on "HeidiSQL" to install. Then create a new session and input a username and password that you'd remember or simply write it down as it is very important to not forget them. Create and connect.
<p>
<p>
<img width="80%" height="1174" alt="slide24" src="https://github.com/user-attachments/assets/88c3a14d-9b0f-4f5c-b89f-55f7d867f026" />
<p>
<p>
Create a database called “osTicket (Click on "Create New")
<p>
<p>
<img width="80%" height="828" alt="slide25" src="https://github.com/user-attachments/assets/ca8e9f66-d16c-4f5f-bb19-21f276e7cb74" />
<p>
<p>
Continue Setting up osTicket in the browser
Go back to the webpage > Go to the database setting > Input all the MySQL information > Click "Install Now" button

Congratulations, hopefully there was no error!!
<p>
<p>
<img width="80%" height="876" alt="slide26" src="https://github.com/user-attachments/assets/e5d2b50d-b74e-40b3-92cb-c63533e063fa" />
<p>
<p>
Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)
<p>
<p>
<img width="3730" height="1826" alt="slide27" src="https://github.com/user-attachments/assets/240e24c8-dc28-4b56-9feb-bd8e8780eebe" />
<p>
<p>
Congrats, You've Finished Installing osTicket.

