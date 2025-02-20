<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Protocol
- Internet Information Services (IIS)
- Chocolatey (package manager and dependency handler and  for Windows)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- php
- php-manager
- mysql
- heidisql
- url rewrite

<h2>Installation Steps</h2>

<p>
  Install chocolatey in powershell with <code>Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))</code>
</p>
  <p></p>and the prerequisites via chocolatey with <code>choco install php php-manager mysql heidisql -y</code>
</p>
<p>
<img src="https://github.com/user-attachments/assets/ca07dbcc-5d89-4b77-9a61-36c6af56533f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Download osTicket with your desired plugns, then extract the upload folder from the archive to C:/inetpub/wwwroot/ and rename it to osticket, and finally extract your .phar plugins to osticket/include/plugins
</p>

<p>
  Rename osticket/include/ost-sampleconfig.php to ost-config.php so it will be read by the site, then disable permission inheritance on ost-config.php and give full permissions to everyone. (This is for convenience during the configuration steps)
</p>
<p>
<img src="https://github.com/user-attachments/assets/da430e69-e548-4f0a-a8ed-b73e23126da6" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/user-attachments/assets/4bbea470-d587-4dbd-96e0-99577e797231" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Register your PHP installation from within IIS and enable the php_opcache and php_intl modules from within IIS (if you miss any then they will show during the initial setup)
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Add osticket as a site in IIS and change the default site if you desire
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Open your site in the web browser via your domain or loopback address
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Fill out the intial setup forms
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Remove write permissions to ost-config.php and set to read only
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
  Delete your setup folder
</p>
<p>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
