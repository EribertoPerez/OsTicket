<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
<p>
This tutorial outlines a brief post-install configuration of the open-source help desk ticketing system osTicket. If you dont have a Virtual Machine 
running osTicket already. Please see the osticket-prereqs for more information on the lab environment.
</p>
<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating System</h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>
<h3>Admin Panel</h3>

- Roles
- Departments 
- Teams
- Agents (workers)
- SLA (Service Level Agreement)
- Help Topics

<h3>Agent Panel</h3>

- Users (Customers)
- Ticket Assignment

<br />
<h2>Admin Panel Configurations</h2>
<h4>Roles</h4>
<p>
Configure roles for agents in the admin panel by navigating to roles and select 'Add New Role' (Admin panel > Agents > Roles > Add New Role). osTicket comes with some default roles, 
but here the role 'Supreme Admin' was created. Whichever agent has this role will have all permissions for tickets, tasks, and knowledgebase.
</p>
<p>
<img height='350' width='500' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/20758a04-d248-4bfc-ba6c-70c98a29e9e5'>
<img height='350' width='500' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/b65a8549-d0a5-436a-9a9b-437882772d9c'>
</p>
<br />
<h4>Departments</h4>
<p>
Configure departments by navigating to departments and selecting 'Add New Department' (Admin panel > Agents > Departments > Add New Department). Here the Department 'System Administrators' was created as an example. Departments are customizable for many businesses needs whether a busness is small or large.
</p>
<p>
<img height='550' width='550' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/a42df551-cc0c-4b03-9bf8-d4f99fc56d76'>
</p>






