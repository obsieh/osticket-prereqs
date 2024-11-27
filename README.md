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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1: Web Server
- Item 2: PHP
- Item 3: Database
- Item 4:Mail Server
- Item 5: osTicket Source Code

<h2>Installation Steps</h2>
Step 1: Set Up the Environment

![image](https://github.com/user-attachments/assets/dc9c36e3-859c-4960-9d4a-e56ba339be45)




</p>
<p>
Install IIS and enable CGI to host the application. Use the provided installation files to install PHP Manager, the Rewrite Module, and VC_redist. Extract PHP 7.3.8 into C:\PHP. Install MySQL and configure it with the root user credentials.
</p>
<br />

Step 2: Configure IIS

![image](https://github.com/user-attachments/assets/b8593d75-8794-47c9-815f-8c0ebb215551)


</p>
<p>
Register PHP in IIS using the PHP Manager and reload IIS. Copy the upload folder from the osTicket installation files to C:\inetpub\wwwroot and rename it to osTicket
</p>
<br />



Step 3: Install osTicket

![image](https://github.com/user-attachments/assets/e35128f4-742d-4ada-9d62-64d80588734c)

<p>
Launch the osTicket setup in your browser via IIS. Enable the required PHP extensions (php_imap.dll, php_intl.dll, and php_opcache.dll). Rename ost-sampleconfig.php to ost-config.php and assign full control permissions to the file.
</p>
<br />
Step 4: Finalize Installation

![image](https://github.com/user-attachments/assets/48aba119-350e-4b0d-8c64-8643b5984c8f)

Use HeidiSQL to create a database named osTicket. Complete the setup in the browser by connecting osTicket to the database and providing helpdesk details. Finally, delete the setup folder and set ost-config.php to read-only.

