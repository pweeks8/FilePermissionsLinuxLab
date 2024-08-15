<h1>File Permissions in Linux</h1>

<h2>Description</h2>

Project consists of updating file permissions for certain files and directories within the projects directory. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep their system secure. 
<br />


<h2>Languages Used</h2>

- <b>Bash</b>

<h2>Environments Used </h2>

- <b>In browser virtual machine</b>

<h2>Lab walk-through:</h2>

<p align="center">
Check file and directory details: <br/>
<img src="https://i.imgur.com/jHkV0KS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
Change file permissions: <br/>
<img src="https://i.imgur.com/7VYagJN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
Change file permissions on a hidden file: <br/>
<img src="https://i.imgur.com/ZMgOQvf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
Change directory permissions:  <br/>
<img src="https://i.imgur.com/evuKeLR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Summary</h2>

- I changed multiple permissions to match the level of authorization my organization wanted for files and directories in the projects directory. The first step in this was using ls -la to check the permissions for the directory. This informed my decisions in the following steps. I then used the chmod command multiple times to change the permissions on files and directories.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
