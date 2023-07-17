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
- SLA (Service Level Agreements)
- Help Topics

<h3>Agent Panel</h3>

- Users (Customers)
- Ticket Assignment

<br />
<h2>Admin Panel Configurations</h2>
<h3>Roles</h3>
<p>
Configure roles for agents in the admin panel by navigating to roles and select 'Add New Role' (Admin panel > Agents > Roles > Add New Role). osTicket comes with some default roles, 
but here the role 'Supreme Admin' was created. Whichever agent has this role will have all permissions for tickets, tasks, and knowledgebase.
</p>
<p>
<img height='350' width='500' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/20758a04-d248-4bfc-ba6c-70c98a29e9e5'>
<img height='350' width='500' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/b65a8549-d0a5-436a-9a9b-437882772d9c'>
</p>
<br />
<h3>Departments</h3>
<p>
Configure departments by navigating to departments and selecting 'Add New Department' (Admin panel > Agents > Departments > Add New Department). Here the Department 'System Administrators' was created. Departments are customizable for many businesses needs whether a busness is small or large.
</p>
<p align='center'>
<img height='550' width='550' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/a42df551-cc0c-4b03-9bf8-d4f99fc56d76'>
</p>
<br />
<h3>Teams</h3>
<p>
Configure Teams by navigating to Teams and selecting 'Add New Team' (Admin panel > Agents > Teams > Add New Team). Here the Team 'Level 2 Support' was created.
Teams allow a business to pull agents from different departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.
</p>
<p align='center'>
<img height='400' width='550' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/3fd407c8-a0cf-4b25-b39c-e842c25c5015'>
</p>
<br />
<h3>Agents</h3>
<p>
Create a new agent account by navigating to Agents and selecting 'Add New Agent' (Admin panel > Agents > Add New Agent). Here a few new Agents that were created and given 
differing Access and Permissions. Access and permissions can be modified at any time and help organize Agents so they have the proper Access or Permission(s).
</p>
<p align='center'>
<img height='450' width='500' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/b19710e6-fdd8-43a9-9456-ac7e3cb244bc'>
<img height='450' width='600' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/b1c8ccb5-7ef7-4a2e-bf5f-2e7bf0ba4d90'>
</p>
<br />
<h3>SLA (Service Level Agreements)</h3>
<p>
Create a new SLA plan by navigating to SLA and selecting 'Add New SLA Plan' (Admin panel > Manage > SLA > Add New SLA Plan). Here a few new SLA Plans that were created and have
differing grace periods and schedules. The purpose of the SLA Plan or Service Level Agreement is to provide a length of time in which the help desk Administrator expects tickets to be closed, but SLA plans can be different and mean different things from company to company.
</p>
<p align='center'>
<img height='350' width='500' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/26ff95e7-5808-42fb-bf1c-47029a3dfef0'>
<img height='200' width='600' src='https://github.com/EribertoPerez/OsTicket/assets/34051119/c153fc5c-f758-409c-95a7-9d2c0a4f42b5'>
</p>
<br />



