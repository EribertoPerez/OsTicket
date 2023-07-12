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
From the PHP Manager select register new PHP version and select the folder we unzipped/downloaded PHP into earlier in the lab. Once finished registering PHP restart IIS so it's 
using the changes we made.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/2131b5ae-0a0d-4666-adfa-1f8323296978" height="400" width="700">
</p>
<br />
<p>
Next, we'll download OsTicket and extract the 'upload' folder into the 'c:\inetpub\wwwroot' folder and rename it 'osTicket' with no spaces.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/3cce9694-20af-4644-a5d2-1034caef8f9e" height="400" width="900">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/c7fef3a4-d730-4230-8440-b88de9ffca22" height="100" width="500">
</p>
<br />
<p>
Open osTicket from the IIS panel by navigating to the osTicket site (Server > Sites > Default Web Site > OsTicket), then on the right hand side click on 'Browse *80' to open OsTicket
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/896fe4ee-27c4-4657-bceb-51a7ddd761fe" height="400" width="500">
</p>
<br />
<p>
Now with OsTicket open in the browser you shold see some of the recommended features aren't enabled, we'll enable those by going to our OsTicket browser folder in IIS and using the PHP 
Manager. Go to enable or disable extentions and enable these extentions; 'php_imap.dil' , 'php_intl.dil' , and 'php_opcache.dil'. After doing this we'll refresh the browser and see that the ones we wnabled turn green.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/7da52cc6-7818-464f-8931-6e2a86a5cc67" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/12f36763-8ca6-48e7-85ae-45ce93a1bafc" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/f120e0a2-38dd-427c-b1f3-81cb3dd975bc" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/3d9233c8-56e2-4309-b3ba-cbb34a255da6" height="400" width="500">
</p>
<br />
<p>
Next, we need to rename and enable permissions for a file in our osTicket folder we renamed earlier (Windows(C:) > inetpub > wwwroot > osTicket > Include > ost.sampleconfig.php). 
First we'll rename the file 'ost.sampleconfig.php' to 'ost.config.php', from there we'll change the permissions on that file to be open to 'everyone' (Properties > Security > Advanced). Disable Inheritance first, then add permissions for everyone.
</p>
<p>
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/e7ab106e-64e9-4b6f-9e17-302f91bc78b0" height="350" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/3a1bbeec-579c-4a55-9330-8e6749fc0186" height="350" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/de33919f-57f6-4bd3-9986-0c8e987d41ce" height="450" width="600">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/f592259a-ba7e-489f-a34f-5462b23a42f6" height="450" width="400">
</p>
<br />
<p>
Now we'll continue with OsTicket in the browser, configure OsTicket with whichever credentials you prefer just make sure you write them down or remember them for later! After
the credentials we need to add our SQL database to OsTicket so we can have a database for our users information. In order to do that we will install HeidiSQL, login with our SQL server credientials we made earlier, and create a new database named osTicket. After setting up our database in HeidiSQL we can input our database information on OsTicket.
</p>
<p align="center">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/43096610-60a3-4c80-819c-1bfb92c0c5e9" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/20953254-7693-4d8f-80cc-ab423fc12f42" height="400" width="500">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/36e6f2da-2532-4669-8e75-bc300fb1d2c3" height="400" width="600">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/25673932-0b27-47f3-88bc-90bbb8b595c5" height="400" width="400">
<img src="https://github.com/EribertoPerez/OsTicket/assets/34051119/153fddc9-f6a5-4c39-a951-ea2851a73fd2" align="center" height="200" width="800">
</p>
<br />
