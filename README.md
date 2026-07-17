<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Enterprise LTSC 2021

<h2>Post-Install Configuration Objectives</h2>

- Access osTicket's Admin, Agent, and End User portals, and understand the distinction between the Agent and Admin panels.
- Configure Roles, Departments, and Teams to structure how agents are organized and permissioned.
- Manage Agent (staff) and User (customer) accounts, and control ticket registration requirements.
- Configure SLA plans to define response and resolution expectations based on severity.
- Configure Help Topics to route incoming tickets to the appropriate department.

<h2>Prerequisite</h2>

- [A fully installed and working instance of osTicket (See my repository on osTicket Installation and Prerequisites)](https://github.com/Praise-Id/osticket-prereqs)

<h2>Configuration Steps</h2>


<h4>
Access the Login Pages.
</h4>

- Open a web browser.
- To log in as an Admin or Agent, go to: http://localhost/osTicket/scp/login.php.
- Enter your admin username and password (created during setup), then click Login.
- To view the End User (customer-facing) portal, open a new tab and go to: http://localhost/osTicket.

<br />

<h4>
Understand Agent Panel vs. Admin Panel.
</h4>

- After logging in at scp/login.php, you'll land in the Agent Panel — this is where agents view, respond to, and manage tickets.
- To access the Admin Panel, look for an "Admin Panel" link, usually found in the top-right navigation bar next to your username.
- Click "Admin Panel" to switch over. This is where you'll configure system-wide settings such as roles, departments, teams, and SLAs.
- You can switch back to the Agent Panel at any time using the corresponding link in the top navigation.

<p>
<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/655bdb89-fd89-4b2f-9323-6ad397362038" />
</p>

<br />

<h4>Configure Roles</h4>
<p>
Roles group together permissions that can be assigned to agents (e.g., what they're allowed to view or do).
</p>

- From the Admin Panel, look at the top navigation bar and click "Agents".
- In the sub-menu that appears, click "Roles" and click the "Add New Role" button.
- In the "Role Name" field, type Supreme Admin (you can name this whatever you want).
- Review the permission checkboxes on this page (organized into tabs like "Tickets," "Knowledgebase," "Miscellaneous"). For a Supreme Admin role, check all available permissions across each tab.
- Click "Add Role" or "Save Changes" at the bottom of the page to save.

<p>
<img width="1242" height="650" alt="image" src="https://github.com/user-attachments/assets/c8cebf96-2251-4c9e-9f2d-4512a95c5e91" />
</p>

<br />

<h4>Configure Departments</h4>
<p>
  Departments control ticket visibility and organize agents into functional groups (e.g., Help Desk, SysAdmins, Networking).
</p>

- From the Admin Panel, click "Agents" in the top navigation.
- Click "Departments" in the sub-menu, click "Add New Department".
- In the "Department Name" field, name the department whatever you want.
- Leave or adjust the "Department Type" (Public or Private) and other default settings as needed.
- Click "Add Department" to save.

<p>
<img width="767" height="788" alt="image" src="https://github.com/user-attachments/assets/63c1fd82-edb9-4406-8ce6-c803917aaa1d" />
</p>

<br />

<h4>Configure Teams</h4>
<p>
 Teams let you pull agents from different departments into a single working group.
</p>

- From the Admin Panel, click "Agents" in the top navigation.
- Click "Teams" in the sub-menu.
- Click "Add New Team".
- Scroll down to the "Team Members" section.
- Use the member selection box to search for and add agents, regardless of which department they belong to.
- Click "Add Team" to save.

<p>
<img width="1192" height="732" alt="image" src="https://github.com/user-attachments/assets/5b3e1f91-23dc-4f3a-8669-beb57c9d2d89" />
</p>

<br />

<h4>Require Registration to Create Tickets</h4>
<p>
  By default, osTicket may allow anyone (even unregistered users) to submit tickets. To require registration:
</p>

- From the Admin Panel, click "Settings" in the top navigation.
- Click "Users" in the sub-menu.
- Locate the setting labelled "Registration" or "Account Registration".
- Find the checkbox for "Unregistered users can create tickets" and uncheck it.
- Ensure the setting reflects "Registration Required" — meaning users must register and log in before creating a ticket.
- Scroll down and click "Save Changes".

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4> Configure Agents (Workers)</h4>
<p>
  Agents are the staff members who will respond to and resolve tickets.
</p>

- From the Admin Panel, click "Agents" in the top navigation.
- Click "Agents" in the sub-menu (this shows the list of existing agents), click "Add New Agent".
- Fill in the required fields (username, first name, last name, email, password).
- In the "Department" dropdown, select a department of your choice.
- Configure any additional fields as needed.
- Click "Add Agent" to save.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>Configure Users (Customers)</h4>
<p>
  Users are the customers who submit support tickets.
</p>

- Log into the Agent Panel (if you're in the Admin Panel, use the link in the top navigation to switch back).
- Click "Users" in the top navigation, click "Add New User".
- Fill in the required fields (name, email, phone, etc.).
- Click "Add User" to save.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4> Configure SLA (Service Level Agreement) Plans</h4>
<p>
  SLAs define response and resolution time expectations for tickets.
</p>

- From the Admin Panel, click "Manage" in the top navigation.
- Click "SLA Plans" in the sub-menu, click "Add New SLA Plan."
- Fill in the required fields.
- you may need to create your schedule first under Manage -> Schedules if it doesn't already exist
- Click "Add SLA Plan" to save.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>Configure Help Topics</h4>
<p>
  Help Topics appear as selectable options when users create a new ticket, helping route tickets appropriately.
</p>

- From the Admin Panel, click "Manage" in the top navigation.
- Click "Help Topics" in the top navigation, click "Add New Help Topic".
- Fill in the required fields.
- Configure the associated department, SLA plan, and priority as appropriate.
- Click "Add Topic" to save.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />
