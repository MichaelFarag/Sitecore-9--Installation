# Prerequisites

1.	MS SQL Server 2016 SP1
2.	MS SQL Management Studio
3.	.Net Framework 4.6.2 or later
4.	Chocolatey [package manager for Windows]
5.	Java Runtime Environment
6.	NSSM
7.	SOLR 6.6.2
8.	Sitecore 9 source  + License

# Steps 

* Please make sure you run CMD or PowerShell run as administrator in all below tasks.

1.	MS SQL Server 2016 SP1.
2.	MS SQL Management Studio.
3.	.Net Framework 4.6.2 or later.
4.	Install Chocolatey from Here, To make sure install correctly by this command choco –v in cmd and give you latest version.
5.	Install Java Runtime Environment by this command choco install javaruntime in cmd,To make sure install correctly by this command java –version and and give you latest version.
6.	Install NSSM package by this command choco install nssm in cmd, To make sure install correctly by this command nssm –v and give you NSSM latest version.
7.	Download Solr 6.6.2 from here, Then Create folder under C:\\ [with name solr-6.6.2] and unzipped Solr source in this folder.
8.	Install Solr by this command nssm install solr in cmd.
9.	Will open prompt window you need to fill data like attached screenshot no.1 & 2 then press enter.
10.	Run Solr by this nssm start solr then browse your Solr from here http://localhost:8983/solr/
11.	Enable Solr SSL to can run Solr as HTTPS. 
12.	Create Folder under C:\\[with name Sitecore] and unzipped attached file [solr-ssl.rar] in this folder.
13.	 Run solr-ssl.ps1 by PowerShell and write this command .\solr-ssl.ps1 -Keystorefile C:\solr-6.6.2\server\etc\solr-ssl.keystore.jks you must see result like attached image no.3.
14.	Open C:\solr-6.6.2\bin then edit in notepad  file  solr.in.cmd by searching on REM Uncomment to set SSL-related system properties then remove word REM That’s before all lines in this section.
15.	Restart Solr by this command nssm restart solr now you can browse your Solr with HTTPS https://localhost:8983/solr/  check attached image no.4.
16.	Download Sitecore 9 source  + License from here
17.	Create folder C:\sitecore\[with name Repository] then unzipped download folder Under this folder.
18.	Update Install.ps1 SQL username and password.
19.	Under this folder run PowerShell as administrator.
20.	Run this command register-PSRepository -Name SitecoreGallaery -Sourcelocation https://sitecore.myget.org/f/sc-powershell/api/v2
21.	Finally run Install.ps1 to start install Sitecore tasks.
