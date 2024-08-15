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

 The first line of the screenshot displays the command I entered, and the other lines display the output. The code lists all contents of the projects directory. I used the ls command with the -la option to display a detailed listing of the file contents that also returned hidden files. The output of my command indicates that there is one directory named drafts, one hidden file named .project_x.txt, and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.
<br />
<br />

<p align="center">
Change file permissions: <br/>
<img src="https://i.imgur.com/7VYagJN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The organization determined that other shouldn't have write access to any of their files. To comply with this, I referred to the file permissions that I previously returned. I determined project_k.txt must have the write access removed for other.
The following code demonstrates how I used Linux commands to do this, the first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. The chmod command changes the permissions on files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. In this example, I removed write permissions from other for the project_k.txt file. After this, I used ls -la to review the updates I made.
<br />
<br />

<p align="center">
Change file permissions on a hidden file: <br/>
<img src="https://i.imgur.com/ZMgOQvf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

The research team at my organization recently archived project_x.txt. They do not want anyone to have write access to this project, but the user and group should have read access. 

The following code demonstrates how I used Linux commands to change the permissions, the first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I know .project_x.txt is a hidden file because it starts with a period (.). In this example, I removed write permissions from the user and group, and added read permissions to the group. I removed write permissions from the user with u-w. Then, I removed write permissions from the group with g-w, and added read permissions to the group with g+r. 
<br />
<br />

<p align="center">
Change directory permissions:  <br/>
<img src="https://i.imgur.com/evuKeLR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

My organization only wants the researcher2 user to have access to the drafts directory and its contents. This means that no one other than researcher2 should have execute permissions.

The following code demonstrates how I used Linux commands to change the permissions, the output here displays the permission listing for several files and directories. Line 1 indicates the current directory (projects), and line 2 indicates the parent directory (home). Line 3 indicates a regular file titled .project_x.txt. Line 4 is the directory (drafts) with restricted permissions. Here you can see that only researcher2 has execute permissions.  It was previously determined that the group had execute permissions, so I used the chmod command to remove them. The researcher2 user already had execute permissions, so they did not need to be added.
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
