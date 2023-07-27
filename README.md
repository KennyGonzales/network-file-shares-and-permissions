<p align="center">
<img src="https://i.imgur.com/6M3dYMZ.png" height="25%" width="25%" alt="Traffic Examination"/>
</p>

<h1>Network-File-Shares-and-Permissions</h1>
In this tutorial, we will be creating some sample file shares with various permissions, attempting to access file shares as a normal user, and creating an "Accountants" security group. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Domain Controller/Client Machine)
- Remote Desktop
- Shared Network Files

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

</p>
<p>
<h2> Tutorial Steps </h2>


<p>
  
In this lab, we will set up shared network files and permissions. We'll create folders on `DC-1` and share them on the network, allowing specific individuals to access certain files. Start by navigating to the **C:/ drive** on `DC-1` and creating four folders: **"read-access"**, **"read/write-access**, **"no-access"**, and **"accounting"**.  
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
After creating the folders, proceed to share them on the network to make them accessible from `Client-1`. Additionally, configure the permissions for each folder in `DC-1`. Set the **"read-access"** folder to **read-only** permissions for domain users, assign **read/write** permissions for domain users to the **"read/write-access"** folder, and grant **read/write** permissions for domain admins only to the **"no-access"** folder.
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
By logging into `Client-1` with a standard user account, we can test the functionality of the shared files we created. It becomes evident that the permissions we configured are functioning correctly.  
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
Return to `DC-1` and navigate to `Active Directory`. Within `Active Directory`, establish a security group named **"Accountants"**. Users assigned to this group will be granted permission to access the **"Accountants"** folder. Access to this folder is _restricted_ to users added to the **"Accountants"** security group, while regular users are _denied_ access.  
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
Write here  
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />
