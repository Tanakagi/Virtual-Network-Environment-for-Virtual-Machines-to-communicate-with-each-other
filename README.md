<h1>Virtual Network Environment for Virtual Machines to communicate with each other</h1>


<h2>Description</h2>
In this project, I used the Azure portal to create a virtual network and two virtual machines that could communicate with each other and could be connected to using (Remote desktop protocol) RDP. 
<br />


<h2>Environments Used </h2>

- <b>Azure Portal</b> 

- <b>Windows Server 2022</b> 

<h2>Program walk-through:</h2>

<p align="center">
 I first started by creating the virtual network in the south africa north region and  named it Vnet1. <br/>
<img src="https://i.imgur.com/rZxUwli.png" height="80%" width="80%" />
<br />
<br />
I then added  an IP address range of 10.1.0.0/16:  <br/>
<img src="https://i.imgur.com/lfqKXlc.png" height="80%" width="80%" />
<br />
<br />
and created a subnet named subnet1 with an IP address space of 10.1.0.0/24: <br/>
<img src="https://i.imgur.com/yDOTxTt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then reviewed and finished the creation of the virtual network:  <br/>
 <img src="https://i.imgur.com/hk1TKqq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Once the virtual network was created, I started the creation of the first virtual machine named VM1:  <br/>
<img src="https://i.imgur.com/z3JOBcf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br /> 
<br />
I then configured the virtual machine (VM1) as follows: 
  <ul>
   <li>To use a Windows-based operating system (Windows Server Datacenter 2022).</li>
   <li>VM1 sizing of Standard_B1 - 1vcpu 1GiB memory.</li>
  </ul>  <br/>
<img src="https://i.imgur.com/TiSFXEw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Created a username named vm1admin and password for VM1:  <br/>
<img src="https://i.imgur.com/Mp0Pavk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 I made sure VM1 was placed on the vnet1 virtual network that I created for this project:  <br/>
<img src="https://i.imgur.com/DfBqRAQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then completed the creation of the virtual machine (VM1):  <br/>
<img src="https://i.imgur.com/D2sU1LT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I started the creation of the 2nd virtual machine, named vm2 using the same steps mentioned above but changed the following:  <br/>
<img src="https://i.imgur.com/6jeS7UK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<ul>
<li> the username of vm2admin and password: </li>
</ul>
<br/>
<img src="https://i.imgur.com/347tLLJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 I then completed the creation of the second virtual machine (vm2):  <br/>
<img src="https://i.imgur.com/BU24Edb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/5SKJbHE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
<br />
Once I completed creating the virtual network, subnet and virtual machines. I tested the connectivity between the virtual machines: <br />

<br />
 I went to VM1 and then selected connect:  <br/>
<img src="https://i.imgur.com/93UohZ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the connect tab I downloaded the RDP file:  <br/>
<img src="https://i.imgur.com/gLUAQNt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 I then opened the RDP file and selected Connect on the prompt:  <br/>
<img src="https://i.imgur.com/BrGiVNM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
and entered the password for VM1:  <br/>
<img src="https://i.imgur.com/PP3bT5K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 I then clicked yes when the following prompt:  <br/>
<img src="https://i.imgur.com/ZZzewZg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 When I connected to VM1 I started disabling the public and private firewalls of VM1 in Windows Defender Firewall settings:  <br/>
<img src="https://i.imgur.com/0C70KRY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the settings, I selected Windows Defender Firewall properties:  <br/>
<img src="https://i.imgur.com/MSozHY2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 I then changed the Inbound setting to allow inbound traffic:  <br/>
<img src="https://i.imgur.com/aIKWoAS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 I also changed the private and public firewall state to off:  <br/>
<img src="https://i.imgur.com/9IeUmYZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
I then repeated the same tasks mentioned above for vm2.
From vm2, I opened up PowerShell and ran the ping command, which was a success.:  <br/>
<img src="https://i.imgur.com/ztX9BeJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
and I did the same from VM1 and got the same results, which resulted in this project being a success:  <br/>
<img src="https://i.imgur.com/IXrAlBd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
