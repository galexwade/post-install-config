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

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Configure Agents (Workers)
- Configure Users (Customers)
- Configure SLA

<h2>Configuration Steps</h2>

<!--- Step 1 -->
<p>
Now that you have finished the installation of osTicket, next we are going to do some configuration. In this first step we are going to create a Supreme Admin <a href="https://docs.osticket.com/en/latest/Admin/Agents/Roles.html">role</a> that will have the ability to do everything in osTicket. So to do this click Admin panel -> Agents -> Roles -> Add New Role. For the name use "Supreme Admin", and assign all permissions available in all three tabs (Tickets, Tasks, and Knowledgebase).
</p>
<p>
<img src="https://i.imgur.com/tFHphEg.png" height="80%" width="80%" alt="Roles in osTicket"/>
</p>
<br />

<!--- Step 2 -->
<p>
Next, we are going to create a <a href="https://docs.osticket.com/en/latest/Admin/Agents/Departments.html">department</a> in osTicket. Click Admin panel -> Agents -> Departments -> Add New Department. For the name use "System Administrators" and leave the rest of the settings as default.
</p>
<p>
<img src="https://i.imgur.com/un5ngPS.png" height="80%" width="80%" alt="Departments in osTicket"/>
</p>
<br />

<!--- Step 3 -->
<p>
Next, we are going to create a <a href="https://docs.osticket.com/en/latest/Admin/Agents/Teams.html">team</a> inside of osTicket. Click Admin Panel -> Agents -> Teams -> Add New Team. For the name use "Level II Support", and leave the rest of the settings default. Under the members tab, add yourself as a team member.
</p>
<p>
<img src="https://i.imgur.com/lB5r3Jn.png" height="80%" width="80%" alt="Teams in osTicket"/>
</p>
<br />

<!--- Step 4 -->
<p>
Next, we are going to allow anyone to create tickets. So go to Admin Panel -> Settings -> User Settings, and then make sure that Registration Required is uncheck (this is important).
</p>
<p>
<img src="https://i.imgur.com/rHcu9cx.png" height="80%" width="80%" alt="User Settings in osTicket"/>
</p>
<br />

<!--- Step 5 -->
<p>
Next, we are going to create some <a href="https://docs.osticket.com/en/latest/Admin/Agents/Agents.html">agents</a>. Click Admin Panel -> Agents -> Agents -> Add New Agent. We're going to create two agents, Jane and John Doe. For the email address for both of these agents use "firstname.lastname@osticket.com" and use "Password1" for the password. Under the Access tab, assign Jane as a System Administrators department with Supreme Admin permissions, assign her to Level II Support team, and give extended access as Support. Assign John Doe to the Support team and with view only permissions.
</p>
<p>
<img src="https://i.imgur.com/NIbAkQh.png" height="80%" width="80%" alt="Agents in osTicket"/>
</p>
<br />

<!--- Step 6 -->
<p>
Next, we are going to create some <a href="https://docs.osticket.com/en/latest/Agent/Users/User%20Directory.html">users</a>. Users are basically the ticket owners of the tickets in the help desk. To do this we're going to need to go into the Agent Panel. Click Users -> Add New User, and we're going to create two users, Karen and Ken.
</p>
<p>
<img src="https://i.imgur.com/LuApyPO.png" height="80%" width="80%" alt="Users in osTicket"/>
</p>
<br />


<!--- Step 7 -->
<p>
Next, we are going to configure SLAs. <a href="https://docs.osticket.com/en/latest/Admin/Manage/SLA%20Plans.html">Service Level Agreements (SLA)</a> are a plan to provide a length of time in which the help desk administrator expects tickets to be closed. To do this we are going to need to go back to the Admin Panel -> Manage -> SLA. We are going to create three SLAs,
</p>

- SEV-A (1 Hour, 24/7) 
- SEV-B (4 Hours, 24/7)
- SEV-C (8 Hours, business hours)

<p>
<img src="https://i.imgur.com/vQjv1fP.png" height="80%" width="80%" alt="Service Level Agreement in osTicket"/>
</p>
<br />

<!--- Step 8 -->
<p>
Lastly, we are going to configure some help topics. <a href="https://docs.osticket.com/en/latest/Admin/Manage/Help%20Topic.html">Help Topics</a> help streamline your end-user's help desk experience to ensure proper assignment and prompt response to the ticket. To do this go to Admin Panel -> Manage -> Help Topics. Create four help topics:
</p>

- Business Critical Outrage
- Personal Computer Issues
- Equipment Request
- Password Reset

<p>
<img src="https://i.imgur.com/RAUeSnP.png" height="80%" width="80%" alt="Help Topics in osTicket"/>
</p>
<br />

<p>
Last part: <a href="https://github.com/galexwade/ticket-lifecycle">osTicket Ticket Lifecycle: Intake through resolution</a>
</p>
