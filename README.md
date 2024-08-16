<h1>DNS Sinkhole + Unbound</h1>

<h2>Description</h2>
Pi-hole is a powerful network-wide ad blocker that functions as a DNS sinkhole, intercepting and blocking advertisements and trackers before they reach any devices on your network. By filtering out unwanted content at the source, Pi-hole not only enhances user privacy and security but also improves overall network performance by reducing unnecessary traffic. The term "sinkhole" refers to its ability to "sink" or redirect unwanted DNS queries, effectively preventing them from reaching their intended destinations. Unbound complements Pi-hole by serving as a validating, recursive DNS resolver. It securely handles and caches DNS queries, further enhancing privacy and ensuring efficient and secure domain resolution.
<br />

<h2>Technology Used</h2>

- <b>Raspberry Pi</b> 
- <b>Ubuntu/Linux</b>
- <b>Network/Router Configuration</b>

<h2>Environments Used </h2>

- <b>Raspberry Pi OS</b>

<h2>Setup Walkthrough</h2>

<p align="center">
First step: image the Raspberry Pi... <br/>
<img src="https://i.imgur.com/TdsZU6R.jpeg" height="100%" width="100%"/>
<br /><br />
Once the Pi is ready to go, install Pi-hole with the following command...  <br/>
<img src="https://i.imgur.com/sssrPRm.jpeg" height="100%" width="100%"/>
<br /><br />
After a successful installation, we set a static IP to the Pi... <br/>
<img src="https://i.imgur.com/MqnnUBv.jpeg" height="100%" width="100%"/>
<br /><br />
In order for the ad-blocking to be applied network-wide, we must set the primary DNS server to the Pi's IP address...  <br/>
<img src="https://i.imgur.com/jmb1D9S.jpeg" height="100%" width="100%"/>
<br /><br />
After applying the changes and restarting the router, we are able to pull up the dashboard - displaying all kinds of information...  <br/>
<img src="https://i.imgur.com/RoV906B.jpeg" height="100%" width="100%"/>
<br /><br />
Now, to install Unbound, use the following command...  <br/>
<img src="https://i.imgur.com/t29d7rF.jpeg" height="100%" width="100%"/>
<br /><br />
Create a configuration file with this command...<br/>
<img src="https://i.imgur.com/pIo0xMc.jpeg" height="100%" width="100%"/>
<br /><br />
Copy and paste this block of code which can be found <a href="https://docs.pi-hole.net/guides/dns/unbound/">here</a>, then save and exit the file...
<img src="https://i.imgur.com/YsdDXlp.jpeg" height="100%" width="100%"/>
<br /><br />
Restart Unbound with the following command...
<img src="https://i.imgur.com/kv04Qwh.jpeg" height="100%" width="100%"/>
<br /><br />
Back in our Pi-hole settings, we want to clear any existing upstream DNS servers and add a new custom one (127.0.0.1#5335 = localhost + port number). We are finished setting up Unbound!
<img src="https://i.imgur.com/DEJArsd.jpeg" height="100%" width="100%"/>
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
