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
<img src="https://imgur.com/AMVvejc.png" height="80%" width="80%" alt="1"/> 

<b>The screenshot captures my command input and its resulting output. I used "ls -la" to list all contents in the projects directory, including hidden files. The output shows one "drafts" directory, one hidden ".project_x.txt" file, and five other project files. The 10-character strings at the start of each line represent file permissions.</b>


2.Change file permissions: <br/>
The organization mandated that "other" users shouldn't possess write access to any files. To adhere to this policy, I revisited the file permissions I had retrieved earlier. It became evident that "project_k.txt" needed its write access revoked for "other" users.<br />
The following code demonstrates how I used Linux commands to do this:<br/>
<img src="https://imgur.com/Mv0a7TR.png" height="80%" width="80%" alt="2"/> 

<b>The screenshot displays my commands and their outputs. Using the "chmod" command, I adjusted file permissions. Specifically, I removed "other" users' write permissions from "project_k.txt". Afterwards, I verified the changes using "ls -la".</b>


3.Change directory permissions:<br/>
To restrict access to the "drafts" directory solely to the "researcher2" user, I employed Linux commands to adjust permissions. Specifically, I ensured that only "researcher2" possesses execute permissions, thereby denying access to others.<br/>
Here's how I implemented the changes:<br/>
<img src="https://imgur.com/Dj6kiKF.png" height="80%" width="80%" alt="3"/> 

In the screenshot, the initial lines showcase the commands I entered, while subsequent lines display the output of the second command. Identifying ".project_x.txt" as a hidden file due to its leading period, I made adjustments to its permissions. Specifically, I revoked write permissions from both the user and group, and additionally granted read permissions to the group. Using "u-w" removed write permissions from the user, "g-w" removed write permissions from the group, and "g+r" added read permissions to the group.<b>

4.Change directory permissions<br/>

To ensure exclusive access for the "researcher2" user to the "drafts" directory and its contents, I executed Linux commands to adjust permissions accordingly. This ensures that only "researcher2" has execute permissions, thereby restricting access to others.<br/>
Below demonstrates the Linux commands utilized to implement these permissions adjustments:<br/>
<img src="https://imgur.com/fpaEJhj.png" height="80%" width="80%" alt="4"/> 

The output provides a listing of permissions for various files and directories. Line 1 represents the current directory ("projects"), while line 2 represents the parent directory ("home"). Line 3 denotes a regular file named ".project_x.txt". Line 4 illustrates the directory ("drafts") with restricted permissions, where only "researcher2" has execute permissions. Since it was decided that the group shouldn't have execute permissions, I utilized the "chmod" command to remove them. As "researcher2" already possessed execute permissions, no further action was required for them.<b>
