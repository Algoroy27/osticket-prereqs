# OsTickets Pre-Reqs 
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

- Azure Virtual Machine 
- Internet Information Services 
- PHP Manager
- Rewrite Module 
- VC Redist
- MySQL
- Heidi SQL
- osTicket v1.15.8





<h2>Installation Steps</h2>

<p>

</p>
<p>
1.) The first thing that we need to do is create a virtual machine. There are many cloud providers that we can use, for this lab, we are going to use Azure (https://portal.azure.com/). We are going to set up a VM with Windows 10 Pro, version 22h2. This machine will have at least 2 vcpus and 16 GB of memory.

2.) Next, connect to the VM via remote desktop(Mac users will have to download Microsoft Remote Desktop from the App Store). You need to get the VM public IP address.  
</p>
<br />

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/7bea9970-016b-44a0-abd1-053f62d7458c)
![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/90598924-4bdb-490e-bfac-911742bf6354)

<p>

</p>
<p>
Once inside the VM, go to the control panel. From the control panel open programs, Select, Turn Windows Features on and off. Then make sure to enable/install IIS in Windows and IIS Management Console. Make sure the following fields are checked; CGI, Common HTTP Features, and ISS Management Console.  
</p>

<br />

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/30294e99-aa1a-4380-9c6a-8b892689a4aa)
![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/33643269-011d-4c0b-b3bf-a89d2e312c7a)
![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/bdf584df-2942-4035-9dd9-11e2e76f3437)

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
