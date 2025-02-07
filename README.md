<h1>Configuring Named Standard IPv4 ACLs</h1>

<h2>Description</h2>
Created a standard named ACL to prevent access to a file server. The file server contains the database for the web applications. Only the Web Manager workstation PC1 and the Web Server need to access the File Server. All other traffic to the File Server were denied.
<br />


<h2>Languages and Utilities Used</h2>

- <b>CLI</b> 


<h2>Environments Used </h2>

- <b>CISCO Packet Tracer</b> 

<h2>Program walk-through:</h2>

- <b>Topology: <b/> 
<br/>
<img src="https://imgur.com/EAZG6jQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>

<br/>
Step 1: Tested network connectivity by pinging other devices on the network. All three workstations are able to ping both the Web Server and File Server:
<br/>
<img src="https://imgur.com/zGXPPEO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />Step 2: Created an ACL on R1 with a statement that permits PC1 (192.168.20.4) and the web server (192.168.100.100) to access the file server (192.168.200.100), all other traffic were denied. Then applied the ACL outbound on the Fast Ethernet 0/1 interface.: <br/>
<img src="https://imgur.com/KosR8dS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />Step 3: Verified ACL configuration and functionality.  PC 0 and PC 2 pings to the File Server was unsuccessful:  
<br/>
<img src="https://imgur.com/E4qGLgZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://imgur.com/NaRYSBi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
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
