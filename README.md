<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute) `Used but not required for osTicket installation`
- Remote Desktop `Used but not required for osTicket installation`

- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2 - x64 Gen2) `Azure Virtual Machine used`

<h2>Post-Install Configuration Objectives</h2>

- [Install PHP Manager for IIS](https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10)
- [Install the Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
- [Install PHP](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
- [Install VC_redist](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
- [Install MySQL](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)

<h2>Configuration Steps</h2>

<p>
<img src="https://imgur.com/43xNgNj.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
The first step would be to enable IIS through windows features.. Bring up your windows search bar by pressing the "win" button on your keyboard and typing in <b> Windows Features </b> like so...
</p>
<br />

<p>
<img src="https://imgur.com/9KEOSwr.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://imgur.com/r3ZV5K1.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>  
</p>
<p>
You would then enable <b>IIS</b> or <b>Internet Information Services</b> by clicking it's box, Afterwards clicking the + drop down box for IIS -> World Wide Web Services -> Application Development Features and enabling CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
