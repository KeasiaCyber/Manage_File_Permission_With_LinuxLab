<h1>File System Permissions Examiner and Modifier</h1>



<h2>Description</h2>
This lab we will showcases a tool developed using bash scripting in a Linux (Unix) environment. The primary objective of this tool is to examine existing permissions on the file system, ensuring alignment with the authorization that should be assigned. In scenarios where permissions are misconfigured, the tool facilitates modification to authorize appropriate users and revoke any unauthorized access.
<br />

<h2>The scenarios given from this lab:</h2>
The research team at my organization needs to update the file permissions for certain files and
directories within the projects directory. The permissions do not currently reflect the level of
authorization that should be given. Checking and updating these permissions will help keep
their system secure.
<br />

<h2>Languages and Utilities Used</h2>

- <b>Bash (Bourne-Again SHell)</b> 


<h2>Environments Used </h2>

- <b>Qwiklabs Virutal Machine</b>

<h2>Program walk-through:</h2>

<p align="center">

  
1.Check file and directory details: <br/>
The following code demonstrates how I used Linux commands to determine the existing
permissions set for a specific directory in the file system.<br />
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

<b>The screenshot captures my command input and its resulting output. I used "ls -la" to list all contents in the projects directory, including hidden files. The output shows one "drafts" directory, one hidden ".project_x.txt" file, and five other project files. The 10-character strings at the start of each line represent file permissions.</b>


2.Change file permissions: <br/>
The organization mandated that "other" users shouldn't possess write access to any files. To adhere to this policy, I revisited the file permissions I had retrieved earlier. It became evident that "project_k.txt" needed its write access revoked for "other" users.<br />
The following code demonstrates how I used Linux commands to do this:<br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 

<b>The screenshot displays my commands and their outputs. Using the "chmod" command, I adjusted file permissions. Specifically, I removed "other" users' write permissions from "project_k.txt". Afterwards, I verified the changes using "ls -la".</b>

