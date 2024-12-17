#<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1- in Windows 1, using server manager.install Active Directory Domain Services
 & Promote as a DC

- Step 2- Now that active directory is installed we will Promote DC1 as a domain controller in whats called a New forest as My domain.com

- Step 3- Within DC-1, In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES” OU named “_ADMINS”

- Step 4- Create a new employee named “Jane Doe” 
<h2>Deployment and Configuration Steps</h2>

- Step 5- Add jane_admin to the “Domain Admins” Security Group

![image](https://github.com/user-attachments/assets/291fa086-ea6c-4893-80b4-e2566e920ddf)
open server manager> Add Roles and Features> next> next> select your Server> find service roles, and click active directory Domain services. hit next until it ask's you to install.




![image](https://github.com/user-attachments/assets/ced2477c-8e33-465f-8b34-094f4c97081c)
Go back to DC-1>Server manager> Locate the triangular image below the flag and click on it. it will say promote the server to a Domain controller. click that and if its successful your computer will Restart



![image](https://github.com/user-attachments/assets/501bdc47-3986-4549-a13e-4600b1daa20b)




After your computer successfully restarts navigate to - windows Adminstrative tools> Active directory users & computers> 



![image](https://github.com/user-attachments/assets/198347f6-5d6c-4638-ba29-573c062e6d50)


Right click My domain> New> Organizational Unit




![image](https://github.com/user-attachments/assets/abb13e25-6dc2-486d-b4a8-3612fa4de598)
name_______ _EMPLOYEES and click OK



![image](https://github.com/user-attachments/assets/ee273f39-e188-412b-b5c9-baaaf36b00a5)
Repeat Process for Creating Admins Organizational unit


![image](https://github.com/user-attachments/assets/fe7e40d2-c173-4e42-bd76-1ee7fc1785c8)
click on Admins> Folder> NEW> User> 


![image](https://github.com/user-attachments/assets/9f1e8ff8-a59b-4c5c-8cf3-61c12cb3272d)
Fill out the users Information 


![image](https://github.com/user-attachments/assets/2ee1b429-01dc-4805-869e-1ca229db3b6f)
Create the users Password



![image](https://github.com/user-attachments/assets/47211951-b11b-423d-b7c9-3bb14bac5c6e)

Navigate to Admins and find janes account. Right Click,Properties > Members of > ADD, write  Domain Admins and check names
