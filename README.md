<p align="center">
<img src="https://i.imgur.com/1FpWBmh.png"/>
</p>

<h1>Security Information and Event Management (SIEM) - Microsoft Sentinel Tutorial with Cyber Attacks - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- MySQL / Heidi SQL
- osTicket Support Ticketing System

<h2>Operating Systems Used</h2>

- Windows 10 (21H2)

<h2>List of Prerequisites</h2>

- Install and configure osTicket (Help Desk Ticketing System)
-
- 
- 
- 
 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/SAGGHCX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Resource Group: Make sure to take note of the region you choose, you will need it again later.
</p>
<br />

<p>
<img src="https://i.imgur.com/XNNZSdE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Virtual Machine
* Select the same resource group name you just created
</p>
<br />

<p>
<img src="https://i.imgur.com/tzdBZd2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In Security Type select Standard
</p>
<br />

<p>
<img src="https://i.imgur.com/NBUQahW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a username and password
Take note of this, you will need it to log into the Virtual Machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/JZ9FPoy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make sure this box is checked off
</p>
<br />

<p>
<img src="https://i.imgur.com/H6TeBAK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next to NIC network security group click Advanced
</p>
<br />

<p>
<img src="https://i.imgur.com/EmQXX9l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This will automatically pre-fill for you
</p>
<br />

<p>
<img src="https://i.imgur.com/u5ThMqp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Create New
</p>
<br />

<p>
<img src="https://i.imgur.com/3s44vAB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the 3 dots to the far right
</p>
<br />

<p>
<img src="https://i.imgur.com/pFNyskp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Remove
</p>
<br />

<p>
<img src="https://i.imgur.com/Ig17R9X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>Click Add an Inbound Rule
</p>
<br />

<p>
<img src="https://i.imgur.com/fhoFdcL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what you will see before you make any changes
</p>
<br />

<p>
<img src="https://i.imgur.com/g4yCS9P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p> Change Priority to 100, and name it DANGER_ANY_IN
</p>
<br />

<p>
<img src="https://i.imgur.com/dyJTTm5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/5KAf0rH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>Click Add
</p>Click Review + create
</p>
<br />

<p>
<img src="https://i.imgur.com/tuQIGZA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
 <p>
<img src="https://i.imgur.com/SBgpkXC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>After you see validation passed, click Create
</p>
<br />

<p>
<img src="https://i.imgur.com/axU0Ay0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>In the search bar type in Log Analytics workspace
</p>
<br />

<p>
<img src="https://i.imgur.com/Dh9CQwv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Create log analytics workspace
</p>
<br />

<p>
<img src="https://i.imgur.com/einKXeo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Choose the same Resource Group you created earlier
</p>
<br />

<p>
<img src="https://i.imgur.com/jgQCEAb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>Enter a name for the log 
</p>Ensure the region is the same as your Resource Group 
</p>
<br />

<p>
<img src="https://i.imgur.com/CAaWqam.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Review + Create
</p>
<br />

<p>
<img src="https://i.imgur.com/C7kbJhL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>You should see Validation passed
</p>
<br />

<p>
<img src="https://i.imgur.com/p7uN3X4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Create
</p>
<br />

<p>
<img src="https://i.imgur.com/H3kYlxV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Type in Security Center in Microsoft Azure: Here you will enable the ability to capture logs from the VM into the log analytics workspace
</p>
<br />

<p>
<img src="https://i.imgur.com/gwG3Yvh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>Click Microsoft Defender for Cloud
</p>
<br />

<p>
<img src="https://i.imgur.com/n8Epg7J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Environment settings
</p>
<br />

<p>
<img src="https://i.imgur.com/GgTbGZy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the drop-down next to Azure Subscription
</p>
<br />

<p>
<img src="https://i.imgur.com/v46iG2j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the log analytics workspace you created
</p>
<br />

<p>
<img src="https://i.imgur.com/SVc7iLb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Turn on Foundational CSPM and Servers
<p>Turn off SQL servers on machines
</p>
<br />

<p>
<img src="https://i.imgur.com/bfHpEO3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Save
</p>
<br />

<p>
<img src="https://i.imgur.com/yGgmtCi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Data Collection
</p>
</p>
<br />

<p>
<img src="https://i.imgur.com/Xy9Lenm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click All Events
</p>
<br />

<p>
<img src="https://i.imgur.com/c0lAido.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Save
</p>
<br />

<p>
<img src="https://i.imgur.com/qix3x3A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Log Analytics Workspaces
</p>
<br />

<p>
<img src="https://i.imgur.com/tiSPU53.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Choose the log you created
</p>
<br />

<p>
<img src="https://i.imgur.com/sSCLnwI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Virtual Machines deprecated
</p>
<br />

<p>
<img src="https://i.imgur.com/XjbUKRx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Choose your virtual machine
</p>
<br />

<p>
<img src="https://i.imgur.com/XUyxiQL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click connect
</p>
<br />

<p>
<img src="https://i.imgur.com/X9Nwez2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Search Microsoft Sentinel in the search bar at the top of the Azure page.
</p>
<br />

<p>
<img src="https://i.imgur.com/aSoneaw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Create Microsoft Sentinel
</p>
<br />

<p>
<img src="https://i.imgur.com/rElHue0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the log you created
</p>
<br />

<p>
<img src="https://i.imgur.com/PT6wqFM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Add 
</p>
</p>
<br />

<p>
<img src="https://i.imgur.com/aOikBjy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Copy the public IP address for your VM
</p>
<br />

<p>
<img src="https://i.imgur.com/VxBCDwq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>If you’re using a MAC Computer, download Microsoft Remote Desktop
</p>
<br />

<p>
<img src="https://i.imgur.com/aBMcCIz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Add  pc
</p>
<br />

<p>
<img src="https://i.imgur.com/2P36nGl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Enter the public IP address of your Virtual Machine
</p>
<br />

<p>
<img src="https://i.imgur.com/jrKTdD8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Add
</p>
<br />

<p>
<img src="https://i.imgur.com/2bnFR2i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Enter a random username and password, and you will see the failed log show up.
</p>
<br />

<p>
<img src="https://i.imgur.com/TlJvzKZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/KNx7bPO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Continue
</p>
<br />

<p>
<img src="https://i.imgur.com/Ds949B7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what it will look like if the login failed
<p>Then enter the correct username and password to get into your Virtual Machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/RKz0QMO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what you should see if you’ve logged into your Virtual Machine successfully.
</p>
<br />

<p>
<img src="https://i.imgur.com/rNgtA2T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Turn all of these to No
</p>
<br />

<p>
<img src="https://i.imgur.com/DHaIM8T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Microsoft Edge
</p>
<br />

<p>
<img src="https://i.imgur.com/u4F7e97.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Start without your data
</p>
<br />

<p>
<img src="https://i.imgur.com/CmtNw4F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Continue without this data
</p>
<br />

<p>
<img src="https://i.imgur.com/Cl2uLWj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Confirm and continue
</p>
<br />

<p>
<img src="https://i.imgur.com/mCkIL31.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click confirm and start browsing
</p>
<br />

<p>
<img src="https://i.imgur.com/BHlUbei.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>In the search bar in your Virtual Machine type in Event Viewer
</p>
<br />

<p>
<img src="https://i.imgur.com/Bd5PHCe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/gIon2lC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Security 
</p>
<br />

<p>
<img src="https://i.imgur.com/jytvFpk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Windows Logs
</p>
<br />

<p>
<img src="https://i.imgur.com/Gvq7iM8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is an example of a login attempt
</p>
<br />

<p>
<img src="https://i.imgur.com/1iKQy6j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Now attempt to log into your virtual machine again but fail on purpose
</p>
<br />

<p>
<img src="https://i.imgur.com/9XaXxqy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Refresh in Event Viewer
</p>
<br />

<p>
<img src="https://i.imgur.com/D9mAtuY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what a failed log-on will look like in Event Viewer
</p>
<br />

<p>
<img src="https://i.imgur.com/xq7FTjs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Notice the fake username you used earlier when you logged in failed.
</p>
<br />

<p>
<img src="https://i.imgur.com/T55mbMo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>In the search bar in your Virtual Machine type in command to bring up the command line.
</p>
<br />

<p>
<img src="https://i.imgur.com/93lITJA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Sz81DMY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Ping the virtual machine public IP Address add a space, then enter -t
</p>
<br />

<p>
<img src="https://i.imgur.com/V8hQECN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>You will see the request time out consistently, you need to turn the firewall off.
</p>
<br />

<p>
<img src="https://i.imgur.com/xurw8A6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>In the search bar in your Virtual Machine type in Firewall
</p>
<br />

<p>
<img src="https://i.imgur.com/97pFUug.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/oNmdqXD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Advanced settings
</p>
</p>
<br />

<p>
<img src="https://i.imgur.com/tPdbCps.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Windows Defender Firewall Properties
</p>
<br />

<p>
<img src="https://i.imgur.com/TJHjilE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click each of these tabs and turn off the firewall
</p>
<br />

<p>
<img src="https://i.imgur.com/8f2ddez.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the drop-down next to firewall state and turn the firewall off
</p>
<br />

<p>
<img src="https://i.imgur.com/9jzDOBK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Apply
</p>
<br />

<p>
<img src="https://i.imgur.com/Sqo5O2A.png)" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Now you should be getting a response in the command line from your virtual machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/sbIdP6j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Go to this link to copy/paste the PowerShell script
</p>
<br />

<p>
<img src="https://i.imgur.com/iXUzPwx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>In the search bar in your Virtual Machine search PowerShell ISE
</p>
<br />

<p>
<img src="https://i.imgur.com/eyi4uRQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/TINkQVA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the blank sheet of paper icon (MEANS "NEW")
</p>
<br />

<p>
<img src="https://i.imgur.com/6wCf13A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Paste the PowerShell script you copied earlier
</p>
<br />

<p>
<img src="https://i.imgur.com/u7KLjsN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Go to this website and create an API key
<p>Choose the paid version ($15) so you can get enough API Requests for the lab
</p>
<br />

<p>
<img src="https://i.imgur.com/zJHlFBi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Enter YOUR API Key in this section in between the quotation marks in the Powershell script
</p>
<br />

<p>
<img src="https://i.imgur.com/cYTKf17.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Save
</p>
<br />

<p>
<img src="https://i.imgur.com/jX1uYks.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Save it on the Desktop
</p>
<br />

<p>
<img src="https://i.imgur.com/lZFYJH5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Name it log_exporter
</p>
<br />

<p>
<img src="https://i.imgur.com/KPeFAGg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Save
</p>
<br />

<p>
<img src="https://i.imgur.com/lwdQQSM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/xqAlJue.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Copy the log file path and enter it into the search bar in your Virtual Machine
</p>
<br />

<p>
<img src="https://i.imgur.com/ZmKZhHX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Go back to the Powershell script and click the green play icon to run the script
</p>
<br />

<p>
<img src="https://i.imgur.com/2dMDpDp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what you should see if everything worked correctly.
</p>
<br />

<p>
<img src="https://i.imgur.com/JUQg41w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>In C:\ProgramData\  click failed_rdp to see the log
</p>
<br />

<p>
<img src="https://i.imgur.com/5zWCB6N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Go to Log Analytics workspaces
</p>
<br />

<p>
<img src="https://i.imgur.com/WnPMcT8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the log analytics workspace you created earlier
</p>
<br />

<p>
<img src="https://i.imgur.com/Nk3PK9U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Tables 
</p>
<br />

<p>
<img src="https://i.imgur.com/rwjI1j7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Create
</p>
<br />

<p>
<img src="https://i.imgur.com/7PjkRws.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Select New custom log (MMA-based)
</p>
<br />

<p>
<img src="https://i.imgur.com/WUswm6q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Dfzn21c.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>If you’re on a Mac computer open pages and  save the log to your computer as a Plain text file
</p>
<br />

<p>
<img src="https://i.imgur.com/VCajC9I.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Save
</p>
<br />

<p>
<img src="https://i.imgur.com/DUNfUDG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Name it logfile
</p>
<br />

<p>
<img src="https://i.imgur.com/187hnKN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Export
</p>
<br />

<p>
<img src="https://i.imgur.com/aoj61Aa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>After that go back to Azure in Log Analytics workspace
 Click your workspace you created
 Click custom logs on the left hand side
 Click add a custom log
 Then click the folder icon
</p>
<br />

<p>
<img src="https://i.imgur.com/Wj3KIH7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Select the text file you just created of your logs
</p>
<br />

<p>
<img src="https://i.imgur.com/ecmOgEu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Next twice
</p>
<br />

<p>
<img src="https://i.imgur.com/pbqUsc0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/fJRfUuF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/4bNVXS6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Next Select Windows, and enter the path of the log file on your Virtual Machine
</p>
<br />

<p>
<img src="https://i.imgur.com/8ntaQZD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Next
</p>
<br />

<p>
<img src="https://i.imgur.com/JCaaDKV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Create a custom log name
</p>
<br />

<p>
<img src="https://i.imgur.com/ptAA559.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click next
</p>
<br />

<p>
<img src="https://i.imgur.com/nGQ6JiW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>You should see all of these with a green checkmark if everything worked correctly
</p>
<br />

<p>
<img src="https://i.imgur.com/AF6XoQp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Create
</p>
<br />

<p>
<img src="https://i.imgur.com/4JOwjNq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>While your custom log is loading you can type in SecurityEvent 
</p>
<br />

<p>
<img src="https://i.imgur.com/2Vw4Zes.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/nNB1bss.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/nQcxWUt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/o0ftYyX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<p>Type in where then follow this path to get to event ID 4625
 Click Run
</p>
<br />

<p>
<img src="https://i.imgur.com/ZuTxAmi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>These are the two incorrect attempts we did earlier
</p>
<br />

<p>
<img src="https://i.imgur.com/kEBYps1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Notice 4625 An account failed to log on
</p>
<br />

<p>
<img src="https://i.imgur.com/jtM9RyZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Try the custom log name  you created earlier FAILED_RDP_WITH_GEO_CL and Click Run
</p>
<br />

<p>
<img src="https://i.imgur.com/MAWB1Oi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>After some time try the custom log you just created and it should bring up activity.
</p>
<br />

<p>
<img src="https://i.imgur.com/KUlSq8U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Setup map in Microsoft Sentinel with latitude and longitude
</p>
<br />

<p>
<img src="https://i.imgur.com/1YHVLA5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click overview
</p>
<br />

<p>
<img src="https://i.imgur.com/mFKSGsb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click workbooks
</p>
<br />

<p>
<img src="https://i.imgur.com/MhimYeW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click add workbook
</p>
<br />

<p>
<img src="https://i.imgur.com/cTVujh3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Edit
</p>
<br />

<p>
<img src="https://i.imgur.com/hb6WmsY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click the 3 dots next to the two default widgets
</p>
<br />

<p>
<img src="https://i.imgur.com/PQFtK0P.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Remove
</p>
<br />

<p>
<img src="https://i.imgur.com/F3FkMad.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click yes
</p>
<br />

<p>
<img src="https://i.imgur.com/HH0dZ2e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Add
</p>
<br />

<p>
<img src="https://i.imgur.com/PmNSg9K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Add query
</p>
<br />

<p>
<img src="https://i.imgur.com/0uScgET.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/T32uTge.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p> Enter this script in the blank field under Log analytics workspace Logs Query
</p>
<br />

<p>
<img src="https://i.imgur.com/I1IPxCi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Run Query
</p>
<br />

<p>
<img src="https://i.imgur.com/9pPvRfR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/XN32UTz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Under Visualization
<p>Click the drop-down and select Map
</p>
<br />

<p>
<img src="https://i.imgur.com/ozG9TM6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what you will see in Map Settings
Make sure color by has even_count selected from the dropdown menu
</p>
<br />

<p>
<img src="https://i.imgur.com/I5gGU0s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Apply
</p>
<br />

<p>
<img src="https://i.imgur.com/TVT581p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Under size for the map click large
</p>
<br />

<p>
<img src="https://i.imgur.com/eW7VGRL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Go back to settings and for metric label select label from the drop-down menu
</p>
<br />

<p>
<img src="https://i.imgur.com/rRsC0fS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Apply
</p>
<br />

<p>
<img src="https://i.imgur.com/cS2M3qL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/3MU06kR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what your map will look like so far, this should be an approximate of your location from the failed logon attempts earlier.
</p>
<br />

<p>
<img src="https://i.imgur.com/zyJTbeV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Save and Close
</p>
<br />

<p>
<img src="https://i.imgur.com/J7bouKZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Save Icon
</p>
<br />

<p>
<img src="https://i.imgur.com/HswAKVr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Name the workbook failed_RDP World Map
</p>
<br />

<p>
<img src="https://i.imgur.com/IzvBzpm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Apply
</p>
<br />

<p>
<img src="https://i.imgur.com/ZRxjJNM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Auto refresh from Off to 5mins
</p>
<br />

<p>
<img src="https://i.imgur.com/0iGs0ft.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Click Apply
Give it about an hour or so to start seeing attacks on your virtual machine
</p>
<br />

<p>
<img src="https://i.imgur.com/tn3GctQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Your location is red because your map settings are based on “event count” and you have the most so far.
</p>
<br />

<p>
<img src="https://i.imgur.com/S2ky8Yv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what the two attempts look like from Belize in PowerShell ICE.
I recommend letting everything sit overnight to really see if more attacks happen….
**Remember to check your cost analysis report in Azure before leaving everything running overnight to ensure the cost is something you’re ok with.**
</p>
<br />

<p>
<img src="https://i.imgur.com/gWZs6N1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This was the result after leaving everything running overnight into the next morning.
</p>*Remember to double-check your cost analysis in Azure**
</p>
<br />

<p>
<img src="https://i.imgur.com/a20Mpfy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/2mPirXK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>Here is an example of some of the newly logged failed attempts in Powershell Ice in your Virtual Machine.
</p>*Remember to close everything, and delete all of your resource groups in Azure to make sure you don’t get any further charges.
</p>
<br />

<p>
<img src="https://i.imgur.com/0taBRhx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>This is what you should see when you click your Resource Group to ensure everything was deleted properly.
</p>
<br />

