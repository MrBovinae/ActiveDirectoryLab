<h1>Active Directory Lab - Vulnerability Management Threat Detection</h1>

<h2>Description</h2>
In this Project, we will discover threats or vulnerabilities within a virtual machine used by an employee.
<br />


<h2>Utilities Used</h2>

- <b>Tenable</b> 
- <b>Powershell</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/c4mlkS6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Create The Agent, in this case the Agent has been set to trigger on the creation of a TXT file, this is done to simulate a Zero Trust Enviornment where the user first enters through a secured gateway and is not expected to put anything on the Machine itself as it natively restricts file creation. Furthermore access to assets is strictly enforced through the (IDP) Identity Access Provider, MFA tokens. .:  <br/>
<img src="https://i.imgur.com/L2tDyvI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Run Tenable through powershell the reason we are running tenable internally instead of through their website is this threat scan is intented to simulate the usual method of breach perfomed in thr background through powershell from a Malfesant operation: <br/>
<img src="https://i.imgur.com/n32MMOh.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm Tenable is running through the program data in the background as we can see a folder has been created based of the preset trigger of a new file:  <br/>
<img src="https://i.imgur.com/jRXeklH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
 In this test, I configured Tenable's Agent Scanner to function as a detection mechanism for unauthorized file creation, specifically focusing on the creation of .txt files. The purpose of this setup is to simulate a Zero Trust access environment, where users are not permitted to store files directly on the virtual machine. Instead, they are expected to interact exclusively with resources through an Identity Provider (IdP).

This scenario models a potential threat vector—such as a user inadvertently interacting with a phishing email, which could result in malicious software being silently executed via PowerShell in the background. The creation of a .txt file in such a case could serve as an indicator of compromise.

I also included a screenshot of the ProgramData directory to highlight hidden or typically unobservable activity, reinforcing the importance of visibility in Zero Trust implementations. Normally, this folder is hidden, making it a common location for malware to persist undetected.
<br />

   Now we wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/d85P68N.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
The process is still running in the background and is visible in the Task Manager:  <br/>
<img src="https://i.imgur.com/uZ7ek6Q.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In the provided screenshot, the Tenable Nessus Agent process is actively running in the background, as shown in the Services panel. This supports the simulated Zero Trust use case, where we assume the user has limited visibility into the system’s internals.

In a properly configured Zero Trust environment, while users might be able to open Task Manager, access to detailed service-level information—such as the Local Services tab—would typically be restricted for non-admin users. This restriction is critical in minimizing unnecessary exposure to system components that could be misused or misunderstood.

Even if such visibility were available, identifying a suspicious or unauthorized process among legitimate ones would be exceptionally difficult. This remains true even for experienced cybersecurity professionals, especially if the malicious process is masquerading as a legitimate service or running with minimal system footprint. This underlines the importance of automated scanning tools, like Tenable, to detect anomalies or unauthorized behaviors that may otherwise go unnoticed.

This scenario demonstrates the value of proactive detection over reactive observation—supporting the Zero Trust principle of "never trust, always verify."
<br />
Observe the Vulnerabilities discovered during the scan. :  <br/>
<img src="https://i.imgur.com/hHevbbG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
