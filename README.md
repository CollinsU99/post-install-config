<p align="center">
<img src="https://i.imgur.com/TDCIttW.png" alt="osTicket logo"/>
</p>

<h1>osTicket: Post-Install Configuration</h1>
This tutorial provides a step-by-step guide to configuring the open-source help desk ticketing system osTicket after it has been installed.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Allow anyone to create tickets
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics

<h2>Configuration Steps</h2>

<p align="center">
<img src="https://i.imgur.com/0VwAM3l.png" alt="osTicket logo"/>
</p>

Go to https://portal.azure.com/ and log into your Azure account.

In the search bar, search for "virtual machine", and click "Virtual machines".

<p align="center">
<img src="https://i.imgur.com/MgpOP7b.png" alt="osTicket logo"/>
</p>

Click "vm-osticket".

<p align="center">
<img src="https://i.imgur.com/giJvEbA.png" alt="osTicket logo"/>
</p>

Copy the Public IP Address, and log into the VM with RDP.

<p align="center">
<img src="https://i.imgur.com/BHgMN7M.png" alt="osTicket logo"/>
</p>

We will login into our osTicket Admin account using this link: http://localhost/osTicket/scp/login.php with the username and password we used when we created our osTicket account.

Open the link in your VM web browser and login.

<p align="center">
<img src="https://i.imgur.com/1YFaZQD.png" alt="osTicket logo"/>
</p>

When you login, you will be on the "Agent Panel" by default. You can switch between "Agent Panel and "Admin Panel.

To log on to the admin panel, click the "Admin Panel" tab at the top right.

NOTE: Admins have full control over the osTicket system. They can add and remove agents, create and manage departments, configure settings, and view all tickets.

NOTE: Agents (helpdesk support specialists) can only view and manage tickets that have been assigned to them or their department. They cannot perform tasks such as adding and removing agents, creating and managing departments, or configuring settings.

<p align="center">
<img src="https://i.imgur.com/VVyoOjL.png" alt="osTicket logo"/>
</p>

We will create a role called "Supreme Admin".

NOTE: Roles in osTicket are used to define the permissions and capabilities that users have within the system.

In AdminPanel, click "Agents", 

<p align="center">
<img src="https://i.imgur.com/7fEJhIl.png" alt="osTicket logo"/>
</p>

Click "Roles"

<p align="center">
<img src="https://i.imgur.com/oNIaMcE.png" alt="osTicket logo"/>
</p>

Click "Add New Role"

<p align="center">
<img src="https://i.imgur.com/XkdMusC.png" alt="osTicket logo"/>
</p>

We will name our new role "Supreme Admin". Click "Permissions"

<p align="center">
<img src="https://i.imgur.com/KlueCg6.png" alt="osTicket logo"/>
</p>

Make sure you check all the permissions in the "Tickets, Tasks, and Knowledgebase" tab. Click "Add Role".

<p align="center">
<img src="https://i.imgur.com/jYyoRZe.png" alt="osTicket logo"/>
</p>

Now we have a role that can pretty much do everything.

<p align="center">
<img src="https://i.imgur.com/Hg2yYvw.png" alt="osTicket logo"/>
</p>

Next, we will configure some Departments.

NOTE: Departments in osTicket are used to organize tickets and support requests.

Click "Departments" tab

<p align="center">
<img src="https://i.imgur.com/PlQe24Z.png" alt="osTicket logo"/>
</p>

Click "Add New Departments"

<p align="center">
<img src="https://i.imgur.com/rYjf3i1.png" alt="osTicket logo"/>
</p>

We will name it "System Administrators". Leave everything else as default and click the "Create Dept" button

<p align="center">
<img src="https://i.imgur.com/l77adSR.png" alt="osTicket logo"/>
</p>

As you can see from the image above, "System Administrators is now on our list of Departments

<p align="center">
<img src="https://i.imgur.com/iSuJ6lh.png" alt="osTicket logo"/>
</p>

Next, we will configure some Teams.

NOTE: Teams in osTicket are a way to group agents together to work on specific projects or issues. 

Click the "Teams" tab. 

<p align="center">
<img src="https://i.imgur.com/cMStehW.png" alt="osTicket logo"/>
</p>

Click "Add New Team".

<p align="center">
<img src="https://i.imgur.com/D9Co89M.png" alt="osTicket logo"/>
</p>

We will name it "Level II Support", and click the "Members" tab

<p align="center">
<img src="https://i.imgur.com/DOd9bu7.png" alt="osTicket logo"/>
</p>

Click "Select Agent", add yourself to the team, and click the "Create Team" tab.

<p align="center">
<img src="https://i.imgur.com/E2S5lFY.png" alt="osTicket logo"/>
</p>

Next, we will allow anonymous users to create tickets.

Move your mouse cursor to the "Settings" tab, and click "Users".

<p align="center">
<img src="https://i.imgur.com/8TgdqRq.png" alt="osTicket logo"/>
</p>

Make sure that "Require registration and login to create tickets" is unchecked, and click "Save changes".

<p align="center">
<img src="https://i.imgur.com/QZrHvDS.png" alt="osTicket logo"/>
</p>

Next, we will configure Agents (helpdesk support specialists).

Click the "Agents" tab and click "Add New Agent"
















