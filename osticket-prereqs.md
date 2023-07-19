<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.
Here is a link to all the downloads required for this lab: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used</h2>

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
1) Start off by logging into your Virtual Machine. Once logged in navigate to Turn Windows Features ON or OFF in the Control Panel where we will enable and configure Internet Information Services (Control Panel > Programs > Turn Windows Features ON or OFF). Once here scroll down to and turn on Internet Information Services (IIS), then within IIS navigate to and check CGI (Internet Information Services > World Wide Web Services > Application Development Features > CGI). Next, backtrack to Common HTTP Features and make sure all features are checked (Internet Information Services > World Wide Web Services > Common HTTP Features).
</p>
<p>
<img height="400" width="450" src="https://github.com/EribertoPerez/OsTicket/assets/34051119/87d16fc5-5ab1-472d-9588-942735a185ba">
</p>
<br />
<p>
2) Download and install PHP Manager for IIS and Rewrite Module.
</p>
<p>
<img height="400" width="450" src="https://github.com/EribertoPerez/OsTicket/assets/34051119/601dd66d-8c23-48ee-9099-2e4bc7e0e640">
<img height="400" width="450" src="https://github.com/EribertoPerez/OsTicket/assets/34051119/b7cf71d3-d0b0-4d87-accd-9ddb1c191a01">
</p>
<br />
<p>
3) Create a new folder on your Windows(C:) drive named PHP and install PHP Version 7.3.8 into it.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/49092da9-d201-41b5-90f0-e889622213b9" height="400" width="450">
</p>
<br />
<p>
4) Download and install the C++ Redistributable and MySQL Server
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/6b2112e8-9ea6-4382-87aa-08a9ae146f88" height="300" width="450">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/cbbae151-267d-4bd2-97e2-5a6dc006021d" height="400" width="450">
</p>
<br />
<p>
5) Configure your SQL server (Make sure to write down or use a username and password you will remember) and finish installing
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/7093c768-1a85-46fd-b7f0-edbbf41f3fa2" height="400" width="450">
</p>
<br />
<p>
6) Register PHP from within IIS by opening IIS as an Admin and navigating to PHP Manager.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/0ad261cf-ae4b-4854-b5b7-dcadad15e6db" height="400" width="700">
</p>
<br />
<p>
7) From the PHP Manager select register new PHP version and select the folder we unzipped/downloaded PHP into earlier in the lab, once finished restart IIS.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/2131b5ae-0a0d-4666-adfa-1f8323296978" height="400" width="700">
</p>
<br />
<p>
8) Download OsTicket and extract the 'upload' folder into the 'c:\inetpub\wwwroot' folder and rename it 'osTicket' with no spaces.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/3cce9694-20af-4644-a5d2-1034caef8f9e" height="400" width="900">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/c7fef3a4-d730-4230-8440-b88de9ffca22" height="100" width="500">
</p>
<br />
<p>
9) Open osTicket from the IIS panel by navigating to the osTicket site (Server > Sites > Default Web Site > OsTicket), then on the right hand side click on 'Browse *80' to open OsTicket
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/896fe4ee-27c4-4657-bceb-51a7ddd761fe" height="400" width="500">
</p>
<br />
<p>
10) Now with OsTicket open in the browser you shold see some of the recommended features aren't enabled, we'll enable those by going to our OsTicket browser folder in IIS and using the PHP Manager. Go to enable or disable extentions and enable these extentions: 'php_imap.dil' , 'php_intl.dil' , and 'php_opcache.dil'. Refresh the browser.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/7da52cc6-7818-464f-8931-6e2a86a5cc67" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/12f36763-8ca6-48e7-85ae-45ce93a1bafc" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/f120e0a2-38dd-427c-b1f3-81cb3dd975bc" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/3d9233c8-56e2-4309-b3ba-cbb34a255da6" height="400" width="500">
</p>
<br />
11) Rename and enable permissions for the file 'ost.sampleconfig.php' in the 'Include' folder in osTicket (Windows(C:) > inetpub > wwwroot > osTicket > Include > ost.sampleconfig.php). 
Rename the file 'ost.sampleconfig.php' to 'ost.config.php', then change the permissions on that file to be open to 'everyone' (Properties > Security > Advanced). Disable Inheritance and add permissions for 'everyone'.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/e7ab106e-64e9-4b6f-9e17-302f91bc78b0" height="350" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/3a1bbeec-579c-4a55-9330-8e6749fc0186" height="350" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/de33919f-57f6-4bd3-9986-0c8e987d41ce" height="450" width="600">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/f592259a-ba7e-489f-a34f-5462b23a42f6" height="450" width="400">
</p>
<br />
<p>
12) Continue with OsTicket in the browser, configure OsTicket with whichever credentials you prefer just make sure you write them down or remember them for later. Add our SQL database to OsTicket by installing HeidiSQL and logging in with our SQL server credientials we made earlier, and create a new database named osTicket. After input our database information on OsTicket.
</p>
<p align="center">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/43096610-60a3-4c80-819c-1bfb92c0c5e9" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/20953254-7693-4d8f-80cc-ab423fc12f42" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/36e6f2da-2532-4669-8e75-bc300fb1d2c3" height="400" width="600">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/25673932-0b27-47f3-88bc-90bbb8b595c5" height="400" width="400">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/153fddc9-f6a5-4c39-a951-ea2851a73fd2" align="center" height="250" width="500">
</p>
<br />
<p>
13) Click install now, it will install if everything was configured correctly. If it doesn't install go back and make sure you didn't skip any steps. If you need assistance feel free
to connect and message me:(www.linkedin.com/in/eriberto-perez-b33b41269) Clean up loose ends by deleting the setup file in our osTicket folder
(Windows(C:) > inetpub > wwwroot > osTicket > setup) and change permissions on the 'ost.config.php' file from earlier to read and execute only.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/dd219a36-847e-41bc-a202-528dd0ca5dc8" height="350" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/36818193-6c14-4f7c-bee0-1858198d0ffc" height="350" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/d99d17e6-9d52-4f23-a780-1a1b396c4a39" height="450" width="600">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/dee81108-9725-4b2e-9829-f7b3f2738da5" height="450" width="400">
</p>
<br />
<p>
14) Log into the admin panel by clicking the 'Your Staff Control Panel' link and entering your Admin credentials you created previously. End users can use the 'Your osTicket URL' link to create and submit tickets.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/0ec99a19-7b25-48a7-b577-7385ecfd1b78" height="225" width="600">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/8b02e66a-b46b-45f0-8baa-5a89b5626e64" height="225" width="400">
</p>
