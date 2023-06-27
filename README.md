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
- Link to downloads: https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6






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
NOTE Make sure all Common HTTP features are checked 
</p>

<br />

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/30294e99-aa1a-4380-9c6a-8b892689a4aa)
![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/33643269-011d-4c0b-b3bf-a89d2e312c7a)
![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/bdf584df-2942-4035-9dd9-11e2e76f3437)

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/a6b2df95-886b-44e7-8c93-71dbd80b8c1e)

<p>
To make sure the IIS is installed/enabled go to a browser of your choice and search for 127.0.0.1 It should look something like this.  
</p>
<p>
  5.) Now that the IIS is enabled, From the Installation Files, download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) Go through the install wizard and complete the install.

6.) Next from the Installation Files, download and install the Rewrite Module (rewrite_amd64_en-US.msi)

7.) Create a folder in the C drive called PHP.

8.) From the Installation Files, download PHP 7.3.8 (php-7.3.88-nts-Win32-VC15-x866.zip) and unzip the contents into C:\PHP

9.) Once you have downloaded and extracted the zip file into the PHP folder on the C drive, download and install the VC_redist.x86.exe from the installation files. Go through the setup wizard to finish setting up and installing the VC_redist.x86.exe.

10.) Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) Run the setup wizard: Typical Setup -> Launch Configuration Wizard (after install) -> Standard Configuration ->

Make the new root password: Password1


</p>

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/eb3e7739-2276-4cd9-9f1d-d1fa5a3583c7)






