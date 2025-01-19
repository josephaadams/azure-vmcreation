<p align="center">
<img src="https://i.imgur.com/5SeOYQQ.png" alt="osTicket logo"/>
</p>

<h1>Virtual Machine (VM) Creation Using Microsoft Azure</h1>
This project demonstrates the steps to set up and install osTicket v1.15.8 on a Windows server environment. The guide includes configuring the necessary prerequisites, installing osTicket, and setting up the database.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure: Hosting the virtual machine.

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

**1. Working Computer with Internet Access** (If you don't know how to create a VM using azure, check out my guide: **********REPLACEEEEE**********)

- Purpose: Host the Windows environment for osTicket.
- Setup: Provision a VM with Windows 10 (21H2) or a compatible server OS.

<h2>Creation Steps</h2>

**1. Install osTicket v1.15.8**
- Unzip osTicket-v1.15.8.zip from the installation files.
- Copy the upload folder to C:\inetpub\wwwroot.
- Rename upload to osTicket.

<img src="https://i.imgur.com/yxkKp2E.png"/>
  
**2. Configure IIS**
- Reload IIS:
- Open IIS.
- Stop and Start the server.
- Go to Sites > Default > osTicket.
- On the right, click “Browse *:80” to open osTicket in your browser.

<img src="https://i.imgur.com/06iSCbJ.png"/>

**3. Enable PHP Extensions**
- In IIS, go to Sites > Default > osTicket.
- Double-click PHP Manager.
- Click “Enable or disable an extension” and enable:
- php_imap.dll
- php_intl.dll
- php_opcache.dll

<img src="https://i.imgur.com/qKDXNtr.png"/>
  
**4. Configure ost-config.php**
- Rename the file:
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Assign permissions:
- Disable inheritance and remove all permissions.
- Add Everyone with Full Control.

  <img src="https://i.imgur.com/N63QY76.png"/>
  
**5. Set Up the Database**
- Install HeidiSQL from the installation files.
- Open HeidiSQL and create a new session (root/root).
- Connect to the session and create a database called osTicket.

<img src="https://i.imgur.com/tlwie81.png"/>
  
**6. Complete osTicket Setup in the Browser**
- Open the osTicket installation page in your browser.
- Provide the following details:
- Helpdesk Name: Choose a name for your help desk.
- Default Email: Specify an email address to receive customer tickets.
- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: root
- Click Install Now!


<p>
<img src="https://i.imgur.com/5TZ1qmz.png"/>
</p>
<p>
Congratulations on the installation of osTicket on your server! If you have any questions please make sure to check out osTickets docs https://docs.osticket.com/en/latest/
</p>
<br />


