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

## Post-Install Configuration Objectives <a id="Post-Install-Configuration-Objectives"></a>

- [Install PHP Manager for IIS](https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10)
- [Install the Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
- [Install PHP](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link)
- [Install VC_redist](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)
- [Install MySQL](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link)

<h2>Configuration Steps</h2>

<p>
The first step would be to enable IIS through windows features.. Bring up your windows search bar by pressing the "win" button on your keyboard and typing in <b> Windows Features </b> and `clicking Turn Windows Features On Or Off`
</p>
<p>
<img src="https://imgur.com/43xNgNj.png" height="60%" width="60%" alt="Pic1"/>
</p>
<br />

<p>
You would then enable <b>IIS</b> or <b>Internet Information Services</b> by clicking it's box, Afterwards clicking the + drop down box for <b>IIS</b> -> <b>World Wide Web Services</b> -> <b>Application Development Features</b> and enabling <b>CGI</b> ... If a prompt comes up asking to restart the computer, let it restart.
</p>
<p>
<img src="https://imgur.com/9KEOSwr.png" height="40%" width="40%" alt="Pic2"/> <img src="https://imgur.com/r3ZV5K1.png" height="40%" width="40%" alt="Pic3"/>  
</p>
<br />

<p>
Once the computer has restarted completely you will now start installing the applications needed for osTicket to funtion.
</p>
<br />

Go ahead and install [PHP Manager for IIS](https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10) and the [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link)
<br />

<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExZjk5YTA2N2JhZDVmZjkzNzI5MGRkMWQ2NWQ4NTg3NGI0NzdjM2ZkYSZjdD1n/DpnKHb9l7GvD2lsvkt/giphy.gif" height="40%" width="40%" alt="GIF 1"/> <img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExNjI2ZjRiYmI1Nzc3MTVhODExMWE0OTY5ZTExYzNlOTM1MzUzZGE2MiZjdD1n/UuGRatqPStuyVClrsY/giphy.gif" height="40%" width="40%" alt="GIF 2"/>
<br />

Now create a folder on one of your drives that will be used for the PHP installation.. For example C:/PHP.. Afterwards, go through the installation of [PHP](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link), typing C:\PHP for where it asks to install the files... You can also just do the latter and File Explorer will create the folder for you.

<img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExZWMxNTI4ODVhODlmOWZiNGY5NzgwNmU2YzE4MjQwMjhjZTVjOWNkNCZjdD1n/SDENhhTqVUoTDvzYwx/giphy.gif" height="60%" width="60%" alt="GIF 3"/>

<br />

You can then install [VC_redist](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link) and [MySQL](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link).. Make sure to select "Typical" setup and "Standard Configuration" for a basic install.

<img src="https://i.imgur.com/ieSuZKh.png" height="50%" width="50%" alt="Pic4"/>

`Don't forget your user and password for MySQL! Your username will be "root" through a standard configuration`

<img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExNmRlYTIwYmU5Zjc4NDdjNjE0ZTQxZTkwODJhMTM1ZjFhMTkzZWRkMCZjdD1n/65AMziKlbmqMUdzImI/giphy.gif" height="40%" width="40%" alt="GIF 4"/>
<br />

At this point we will use windows search to open up IIS as administrator shown below...

<img src="https://i.imgur.com/DkDed29.png" height="60%" width="60%" alt="Pic5"/>

Then clicking
- "PHP Manager"
<img src="https://i.imgur.com/McBmbxJ.png" height="100%" width="100%" alt="Pic6"/>
- "Register new PHP Version"
<img src="https://i.imgur.com/fWhi5wO.png" height="50%" width="50%" alt="Pic7"/>

And browsing to the PHP-CGI.exe in your PHP folder to select as the PHP version for IIS.
<img src="https://i.imgur.com/URJylZk.png" height="50%" width="50%" alt="Pic8"/>



Restart your server and install [osTicket](https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view)

Rename the folder "upload" to "osTicket" and copy paste it to \wwwroot folder located in c:\inetpub\wwwroot
<br />



