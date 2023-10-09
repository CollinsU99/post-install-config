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

<h2>High-Level Steps</h2>

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

In Admin Panel, click "Agents", 

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

Click the "Agents" tab and click "Add New Agent".

<p align="center">
<img src="https://i.imgur.com/89kf43w.png" alt="osTicket logo"/>
</p>

Create Jane Doe's account as shown in the image above, and click "Set Password".

<p align="center">
<img src="https://i.imgur.com/UAV9T8o.png" alt="osTicket logo"/>
</p>

Uncheck "Send the agent a password reset email", use "Password1" as Jane Does's password, and uncheck "Require password change at next login" (I mistakenly checked it in the image above). Click "Set"

<p align="center">
<img src="https://i.imgur.com/YfqDAwU.png" alt="osTicket logo"/>
</p>

Click the "Access" tab, and select "System Administrators" for Departments and "Supreme Admins" for Role. Click the "Teams" tab

<p align="center">
<img src="https://i.imgur.com/V7VDWwb.png" alt="osTicket logo"/>
</p>

In the Teams section, select "Level II Support" team, and click the "Create" button

<p align="center">
<img src="https://i.imgur.com/doDJYHW.png" alt="osTicket logo"/>
</p>

Let's add John Wood as an agent. Click "Agents" > "Add New Agent".

<p align="center">
<img src="hhttps://i.imgur.com/7U8XPyp.png" alt="osTicket logo"/>
</p>

Fill in his information as shown in the image above and click "Set Password".

<p align="center">
<img src="https://i.imgur.com/UAV9T8o.png" alt="osTicket logo"/>
</p>

Uncheck "Send the agent a password reset email", use "Password1" as Jane Does's password, uncheck "Require password change at next login", and click "Set".

<p align="center">
<img src="https://i.imgur.com/1gqn2FV.png" alt="osTicket logo"/>
</p>

Click the "Access" tab, select "Support" for Departments, "View only" for Role, "Support" for Extended Access and click the "Create" tab

<p align="center">
<img src="https://i.imgur.com/3GnKY9V.png" alt="osTicket logo"/>
</p>

Next, we will configure users (customers).

Click on the "Agent Panel" tab at the top right of the page.

<p align="center">
<img src="https://i.imgur.com/hu2Iojo.png" alt="osTicket logo"/>
</p>

Click "Users" tab.

<p align="center">
<img src="https://i.imgur.com/RS0sGqn.png" alt="osTicket logo"/>
</p>

Click "Add User".

<p align="center">
<img src="https://i.imgur.com/2ouPdxU.png" alt="osTicket logo"/>
</p>

Let's add Karen Mil as a user. Fill in Karen's informations as shown in the image above, and click "Add User" button

<p align="center">
<img src="https://i.imgur.com/LSAhfxf.png" alt="osTicket logo"/>
</p>

Click "Users".

<p align="center">
<img src="https://i.imgur.com/uv9FExV.png" alt="osTicket logo"/>
</p>

Click "Add User".

<p align="center">
<img src="https://i.imgur.com/msxVoZf.png" alt="osTicket logo"/>
</p>

Let's add Ken Dei as a user. Fill in Ken's informations as shown in the image above, and click "Add User" button

<p align="center">
<img src="https://i.imgur.com/eZ0llEF.png" alt="osTicket logo"/>
</p>

Next, we will configure SLAs

NOTE: SLAs (Service Level Agreement) are used to define the amount of time that it should take to respond to and resolve tickets.

Click the "Admin Panel" tab at the top right of the page.

<p align="center">
<img src="https://i.imgur.com/Mdd5RmN.png" alt="osTicket logo"/>
</p>

Move the cursor to the "Manage" tab and click "SLA". We will go ahead and create three SLAs.

<p align="center">
<img src="https://i.imgur.com/y0EHfqB.png" alt="osTicket logo"/>
</p>

Click "Add New SLA Plan".

<p align="center">
<img src="https://i.imgur.com/wXTIauI.png" alt="osTicket logo"/>
</p>

We will name our first SLA "SEV-A", with 1 hour grace period, select "24/7" for Schedule, and click "Add Plan".

<p align="center">
<img src="https://i.imgur.com/3S5v8eK.png" alt="osTicket logo"/>
</p>

Let's add our second SLA plan. Click "Add New SLA Plan".

Name it "SEV-B", with 4 hour grace period, select "24/7" for Schedule, and click "Add Plan".

<p align="center">
<img src="https://i.imgur.com/7cgiq13.png" alt="osTicket logo"/>
</p>

Let's add our third SLA plan. Click "Add New SLA Plan".

Name it "SEV-C", with 8 hour grace period, select "Monday - Friday" for Schedule, and click "Add Plan".

![2023-10-09 00_18_34-20 125 139 181 - Remote Desktop Connection](https://github.com/CollinsU99/post-install-config/assets/124742607/6b3be3df-8c08-41ee-9655-1f7f665160e7)

Next, we will configure help topics. 

Click "Manage" > "Help Topics"








































