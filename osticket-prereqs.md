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

- Virtual Machine running Windows 10 or greater
- Remote Desktop Software (If not pre-installed on your computer)
- Internet Information Services (IIS)
- PHP manager for IIS
- Rewrite Module
- PHP Version 7.3.8
- C++ Redistributable
- MySQL Server
- OsTicket Version 1.15.8
- HeidiSQL Database Client

<h2>Installation Steps</h2>
<p>
Start off by logging into your Virtual Machine running Windows 10 or greater. Once logged in navigate to Turn Windows Features On or OFF in the Control Panel where we will enable and configure Internet Information Services (Control Panel > Programs > Turn Windows Features On or Off). Once here scroll down to and turn on Internet Information Services, then within IIS navigate to and check CGI (Internet Information Services > World Wide Web Services > Application Development Features > CGI). Next, backtrack to Common HTTP Features and make sure all features are checked (Internet Information Services > World Wide Web Services > Common HTTP Features). Once everything is enabled click ok to apply the changes you've made.
</p>
<p>
<img height="400" width="450" src="https://github.com/EribertoPerez/OsTicket/assets/34051119/87d16fc5-5ab1-472d-9588-942735a185ba">
</p>
<br />
<p>
Next, download and install PHP Manager for IIS and Rewrite Module.
</p>
<p>
<img height="400" width="450" src="https://github.com/EribertoPerez/OsTicket/assets/34051119/601dd66d-8c23-48ee-9099-2e4bc7e0e640">
<img height="400" width="450" src="https://github.com/EribertoPerez/OsTicket/assets/34051119/b7cf71d3-d0b0-4d87-accd-9ddb1c191a01">
</p>
<br />
<p>
Next, Create a new folder on your main drive named PHP and install PHP Version 7.3.8 into it.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/49092da9-d201-41b5-90f0-e889622213b9" height="400" width="450">
</p>
<br />
<p>
Next, download and install the C++ Redistributable and MySQL Server
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/6b2112e8-9ea6-4382-87aa-08a9ae146f88" height="300" width="450">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/cbbae151-267d-4bd2-97e2-5a6dc006021d" height="400" width="450">
</p>
<br />
<p>
Next, configure your SQL server (Make sure to write down or use a username and password you will remember!!!) and finish installing
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/7093c768-1a85-46fd-b7f0-edbbf41f3fa2" height="400" width="450">
</p>
<br />
<p>
Next, we will register PHP from within IIS. Start with opening IIS as an Admin and navigate to PHP Manager.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/0ad261cf-ae4b-4854-b5b7-dcadad15e6db" height="400" width="700">
</p>
<br />
<p>
From the PHP Manager select register new PHP version and select the folder we unzipped/downloaded PHP into earlier in the lab.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/2131b5ae-0a0d-4666-adfa-1f8323296978" height="400" width="700">
</p>


