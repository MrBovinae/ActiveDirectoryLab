<h1>Active Directory Lab - Vulnerability Management Threat Detection</h1>

<h2>Description</h2>
In this Project, we will discover threats or vulnerabilities within a virtual machine used by an employee.
<br />


<h2>Utilities Used</h2>

- <b>Tenable</b> 
- <b>Tenable</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/c4mlkS6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create The Agent:  <br/>
<img src="https://i.imgur.com/L2tDyvI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run Tenable through powershell the reason we are running tenable internally instead of through their website is this threat scan is intented to simulate the usual method of breach perfomed in thr background through powershell from a Malfesant operation: <br/>
<img src="https://i.imgur.com/n32MMOh.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm Tenable is running through the program data in the background as we can see a folder has been created:  <br/>
<img src="https://i.imgur.com/jRXeklH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
