<h1>SIEM with Azure Sentinel Home Lab</h1>


<h2>Description</h2>
I setup Microsoft Sentinel (SIEM) and connected it to a live virtual machine acting as a honey pot to observe live attacks (RDP Brute Force) from all around the world. And I mapped the attacks on Azure Sentinel Map
<br />


<h2>Languages and Utilities Used</h2>

- <b>Powershell</b> 
- <b>Azure Virtual Machine</b>
- <b>Microsoft Sentinel</b>
- <b>Kusto Query Language - KQL</b>



<h2>Environments Used </h2>

- <b>Microsoft Azure Subscription</b> 

<h2>Program walk-through:</h2>

<p align="center">
Created a Windows Virtual Machine (VM) within my Azure subscription and configured the VM to act as a honeypot. 
Then I executed a PowerShell script on the honeypot to extract failed Remote Desktop Protocol (RDP) login attempts.
  <br/>
<img src="img/Screenshot 2023-08-23 165903.png" height="80%" width="80%" alt="without_rsa_module"/>
<br />
<br />
<br />
<br />
Integrated the honeypot VM with Azure Log Analytics Workspace.
Configured the PowerShell script to collect and send logs related to failed RDP login attempts to the Log Analytics Workspace.
Used the API from ipgeolocation.io to get the geological location of the attackers.<br/>
<img src="img/Screenshot 2023-08-23 171829.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <img src="img/Screenshot 2023-08-23 171029.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br />
<br />
<br />
<br />
Utilized Microsoft Sentinel workbook to display the global attack data(RDP brute force) on a world map according to the physical location and thr magnitude of attacks
<img src="img/Screenshot 2023-08-23 171309.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
