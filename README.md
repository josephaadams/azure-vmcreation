<p align="center">
<img src="https://i.imgur.com/5SeOYQQ.png" alt="osTicket logo"/>
</p>

<h1>Virtual Machine (VM) Creation Using Microsoft Azure</h1>
This guide walks you through the step-by-step process of creating a Virtual Machine (VM) in Microsoft Azure under a specific resource group.<br />


<h2>What is a Resource Group?</h2>
A Resource Group is a container in Azure that holds related resources for an Azure solution. These resources could include Virtual Machines (VMs), storage accounts, virtual networks, and more.

<h2>Why Should You Use a Resource Group?</h2>

- Organization: Resource groups make it easy to group and manage resources that belong to the same project or workload.

Example: All resources for a web application (VM, database, storage) can be grouped together in one resource group.

- Access Control: You can assign role-based access to a resource group, controlling who can manage the resources within it.

- Cost Management: Resource groups provide a clear view of costs for all the resources within them. This helps you monitor and optimize spending.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure: Hosting the virtual machine.

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

**1. Working Computer with Internet Access** 

**2. An active Azure account. If you don't have one, create a free account here:(https://azure.microsoft.com/en-us/)**

**3. A resource group already created in Azure. If not, follow these steps:**
- Go to Resource Groups in the Azure portal.
- Click + Create.
- Provide a name, select a region, and click Review + Create.

<h2>Creation Steps</h2>

**1. Sign in to the Azure Portal**
- Navigate to Azure Portal.
- Log in with your Azure account credentials.

<img src="https://i.imgur.com/yxkKp2E.png"/>
  
**2. Navigate to "Virtual Machines"**
- In the left-hand navigation panel, select Virtual Machines. If you don’t see it, search for "Virtual Machines" in the search bar at the top.
- Click on the + Create button and select Azure Virtual Machine.

<img src="https://i.imgur.com/06iSCbJ.png"/>

**3. Basic Configuration**
- Resource Group: Select the resource group we created on the prerequesites.
- Virtual Machine Name: Enter a unique name for your VM. 
- Region: Choose the closest data center for your needs.
- Image: Select the operating system for your VM, in this case we can use Windows 10 Pro.
- Size: Pick the size of your VM based on your workload. You can choose Standard 2 vcpus if you are unsure.

<img src="https://i.imgur.com/qKDXNtr.png"/>
  
**4. Setup your Administrative Account**
- Username: Create a username to log into the VM.
- Password: Enter a secure password. 
-Tip: You can save these details into a notepad and save it n your Desktop just in case you forget them.

<img src="https://i.imgur.com/T4KyBTx.png"/>
 
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


