# IDS/IPS with Suricata


 ### [Project Objectives](https://docs.google.com/document/d/1Ri-dS44i_eEgwXVdjWkTxZXcItDg-ge4/)

<h2>Description</h2>
Project consists of simple install, configure, and test Opnsense IDS/IPS with Suricata
<br />


<h2>Languages and Utilities Used</h2>

- <b>Opensense</b> 
- <b>Multi LAN Environment</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>(21H2)
-  <b>Kali Linux Virtual Machine</b>
- <b>Metasploitable 2.0 Linux</b>


<h2>Program walk-through:</h2>

<p align="center">
Set Kali Linux on the guest network: <br/>
<img src="https://i.imgur.com/vzclhXf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Go to Kali Linux and make sure that you are on the network by running ifconfig:  <br/>
<img src="https://i.imgur.com/5v4b874.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After logging in as root you should be able to run ifconfig.
We see here that we are indeed on the guest network as shown by the IP being 192.168.3.11
: <br/>
<img src="https://imgur.com/HyHv0oD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Set Metasploitable on the LAN network.
:  <br/>
<img src="https://imgur.com/kOYRCCQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  Check package; Suricata
:  <br/>
<img src="https://imgur.com/VkzlDRy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure IDS.
:  <br/>
<img src="https://imgur.com/B6obZz4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select all and click Enable Selected
Then Download & Update Rules
:  <br/>
<img src="https://imgur.com/2JDUqz7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
You will see some have already been enabled by default.
:  <br/>
<img src="https://imgur.com/oqHAFoZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
We will run nmap -A 192.168.2.11 which performs an aggressive scan of the IP.
:  <br/>
<img src="https://imgur.com/cxDeC3f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Go to Kali linux

Run the exploit
:  <br/>
<img src="https://imgur.com/qHOXQ8R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
We can now see that the attack was blocked successfully:  <br/>
<img src="https://imgur.com/uytfaT7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
