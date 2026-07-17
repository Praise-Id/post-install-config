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

- Open a web browser
- To log in as an Admin or Agent, go to: http://localhost/osTicket/scp/login.php
- Enter your admin username and password (created during setup), then click Login.
- To view the End User (customer-facing) portal, open a new tab and go to: http://localhost/osTicket
  
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>
Understand Agent Panel vs. Admin Panel.
</h4>

- After logging in at scp/login.php, you'll land in the Agent Panel — this is where agents view, respond to, and manage tickets.
- To access the Admin Panel, look for an "Admin Panel" link, usually found in the top-right navigation bar next to your username.
- Click "Admin Panel" to switch over. This is where you'll configure system-wide settings such as roles, departments, teams, and SLAs.
- You can switch back to the Agent Panel at any time using the corresponding link in the top navigation.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>Configure Roles</h4>
<p>
Roles group together permissions that can be assigned to agents (e.g., what they're allowed to view or do).
</p>

- From the Admin Panel, look at the top navigation bar and click "Agents".
- In the sub-menu that appears, click "Roles", click the "Add New Role" button 
- In the "Role Name" field, type Supreme Admin (you can name this whatever you want).
- Review the permission checkboxes on this page (organized into tabs like "Tickets," "Knowledgebase," "Miscellaneous"). For a Supreme Admin role, check all available permissions across each tab.
- Click "Add Role" or "Save Changes" at the bottom of the page to save.

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>Configure Departments</h4>
<p>
  Departments control ticket visibility and organize agents into functional groups (e.g., Help Desk, SysAdmins, Networking).
</p>

- 

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h4>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</h4>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />
