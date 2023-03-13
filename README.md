<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.osTicket is a widely-used open source support ticket system which seamlessly integrates inquiries created via email, phone and web-based forms into a simple easy-to-use multi-user web interface. It can manage, organize and archive all your support requests and responses in one place while providing your customers with accountability and responsiveness.<br />


<h2>Video Demonstration</h2>

- ### [ How To Setup a Resource Group](https://loom.com/share/a4b3e70ccf6246aa89bed4496dea9a86)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create the environment using Azure
- Install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Install Rewrite Module (rewrite_amd64_en-US.msi)
- Create a directory c:\PHP
- Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
<a href="https://imgur.com/hSxWqeY"><img src="https://i.imgur.com/hSxWqeY.png" title="source: imgur.com" /></a>
  
- Download and install VC_redist.x86.exe
- Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
- Download and install HeidiSQL
</p>
  
<h2>Installation Steps</h2>
  
<p>
<a href="https://imgur.com/PVgbFv2"><img src="https://i.imgur.com/PVgbFv2.png" title="source: imgur.com" /></a>
</p>
  
<p>
In order to set up the ticketing system, we first have to create the environment in Azure which includes resource group, virtual network, subnet and virtual machine. To ensure that it is properly setup, we set up a network watcher and look at the topology. Then once that is done we enter the virtual machine and setup the prerequisites for osTicket.
</p>
<br />

<p>
<a href="https://imgur.com/VCKgUVs"><img src="https://i.imgur.com/VCKgUVs.png" title="source: imgur.com" /></a>
</p>
<p>


- So after setting up the IIS, we check that it is working properly by doing the 127.0.0.1 localhost loopback.
  
<a href="https://imgur.com/Ovs3XN8"><img src="https://i.imgur.com/Ovs3XN8.png" title="source: imgur.com" /></a>
</p>
<br />

<p>
<a href=[image](https://user-images.githubusercontent.com/119722049/224799237-0b9df0bf-ec78-4cba-8117-a9a95925549b.png) /></a>


- Next download osTicket, extract the content to the folder c:\inetpub\wwwroot. Rename the folder "Upload" to "osTicket".
<a href="https://imgur.com/CKGlNgM"><img src="https://i.imgur.com/CKGlNgM.png" title="source: imgur.com" /></a>
</p>
<p>

- Install current version of osTicket. -Extract and xopy "upload" folder to C:\inetpub\wwwroot. -Within C:\inetpub\wwwroot change "upload" to "osTicket".

- Go to sites, Default, osTicket. -Look on the right side of the IIS screen. Click "Browse*80".
  
 <a href="https://imgur.com/uYUSqaP"><img src="https://i.imgur.com/uYUSqaP.png" title="source: imgur.com" /></a>

- Open PHP Manager. -Enable: php_imap.dll, php_intl.dll, php_opcache.dll -Refresh the osTicket on your browser to see the changes.

- Open C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php -Change ost-sampleconfig.php to ost-config.php.

- Right click ost-config then select Properties. -Disable inheritance then remove all. -New permissions, give to "Everyone", select all.

- Set up your osTicket in your browser. Scroll to the bottom of the osTicket page in your browser and fill in the remaining boxes.

- Open Heidi SQL -Create new session, root/Password1. -Connect to session. -Create a database called "osTicket".

- Continue setting up osTicket in the browser. -Enter MYSQL information.

- Select continue. -A "Congratulations" message should show on your screen.
  
  <a href="https://imgur.com/jD7ZQ1c"><img src="https://i.imgur.com/jD7ZQ1c.png" title="source: imgur.com" /></a>
</p>
<br />
