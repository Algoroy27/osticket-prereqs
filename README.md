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

Execute the process on the next page

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/ca5cb469-c055-4501-af7b-7c50fd901d09)

11.) Now that we have the files downloaded and installed we will want to search for IIS in the windows search bar. Open IIS as an administrator. The program should look like this.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/aa01ca4e-192f-43e1-87af-514c57c4783a)

12.) We will now want to register PHP from within IIS. Click on PHP Manager

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/58f5da05-1b3c-4293-9c55-7bebb15c2947)

Register new PHP version.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/ef20823f-b371-45b1-b2a3-a7552bfbb988)

You will want to provide a path to the php executable file (php-cgi.exe)). Go to C Drive -> PHP -> click on php-cgi file.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/1f598bf9-e7fa-44db-81f9-27cc44c7c582)

Restart the IIS server.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/96011ade-1c5c-4bf6-83c0-b01e9554ffb1)

13.) Install osTicket v1.15.8 -Download osTicket from the Installation Files Folder -Extract and copy "upload" folder to c:\inetpub\wwwroot -Within c:\inetpub\root, Rename "upload" to "osTicket"

Reload IIS again.

14.) On IIS go to sites -> Default -> osTicket -On the right, click “Browse *:80”

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/380606cc-b199-48ff-b298-f8d0f422865f)

Some extensions are not enabled on the osTicket browser. To enable the extensions: -Go back to IIS, sites -> Default -> osTicket -Double click PHP manager -Click "Enable or disable an extension"

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/1dd09fb2-130c-41e6-8c98-50bd834b91b1)

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/e57accd9-a88f-40c7-b804-33eb7c844757)

We will want to enable three extensions from here.

1.) php_imap.dll

2.) php_intl.dll

3.) php_opcache.dll

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/f5961115-a317-4cd3-aeb7-4c15ea86d813)

15.) Once we have those extensions enabled in IIS, we are going to want to rename one of the files in our osTicket folder. Go into the file explorer and search for C;\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

We are going to rename the ost-sampleconfig.php to ost-config.php

Now that we have renamed the files, right-click on the file and go to properties. From there click security, click on advance, and disable the inheritance. We will select Remove all inherited permissions from this object.

Now we will add new permissions.

Click Add

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/2a21aa25-d47e-496a-8d89-cbd8d98a1969)

Select a principal

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/77bf1091-644e-402d-a23a-24360f2e88e0)

Type "Everyone" in the box.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/8d65f6ff-b360-4bc1-a65a-abb11b4ee882)

Make sure Full Control and all the other boxes are checked.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/42617961-0148-4d16-90ad-a445ce2b88bf)

Click Apply and Ok.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/096550a3-eb14-490a-b01a-4a42fe6e4f36)

Once that is done we will continue to setup osTicket in the browser. Click Continue on the osTicket browser page. Fill out the page as required except for the Database Settings at the bottom of the page. We will get to that.

We will want to download and install HeidiSQL from the Installation Files.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/bea9be53-299b-4229-a1c7-859b7f2cf1fc)

When the program is open we will create a new session in it. We want to make sure the username is root and the password is Password1.

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/84284096-4f89-4738-9fcf-f367607c673b)

Once we are connected to the session we will go back to the browser to finish setting everything up. Under the Database Settings in the browser the username will be root and the password will be Password1.

We will now create a new database within HeidiSQL. In Heidi right click on the left side where it says "Unnamed", select "create new", and then select "Database". Name the new database osTicket. Once we have the new database setup go back to the osTicket browser and under MySQL Database type in osTicket.

The last step is to do some cleanup. We will want to delete the setup folder in our system. -Delete: C:\inetpub\wwwroot\osTicket\setup Only delete the setup folder and nothing else.

We then will want to set the permissions back to "Read" only in the ost-config.php file.

Now osTicket is ready for use and you can login with your admin creds. Congrats 

![image](https://github.com/Algoroy27/osticket-prereqs/assets/137920855/8c0c266f-b45a-4e3b-b9ff-50a5082947f1)







