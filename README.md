<h1>Security File Share </h1>
We will create a security group for accountants from the DC-Server and assign “bek.laxe” as a member of the group. Then we will log into the client account to access the security file.<br />

<h2>Prerequisite </h2>
- Completion of the previous lab (https://github.com/SedinamA/AD-setup)

<h2>Environment and Technology used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Service
- Run app

<h2>Operating Systems Used </h2>

- HP Windows 11 laptop (Base Computer)
- Windows Server 2022 Virtual Machine
- Windows 10 Virtual Machine

<h2>Demonstration </h2>

Log into DC-Server as jane.admin. On the C:\ Drive, create a folder named “Accounting”
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/05e73f5c-569e-4526-a12b-c086b6fba269)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/806da8c2-3b9d-4c03-b8e4-1b3d3cc98bac)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/b8b3eaf0-7c33-40a4-b598-ac3b7e5d7ff7)

In the Active Directory, create a security group called “ACCOUNTANTS”
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/29ff98fe-65aa-4481-bb2e-8ac0bae56ca8)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/068050ab-3323-45a4-97f8-7316dfa0e9fd)

On the “accounting” folder set the permissions that follow; Folder-accounting, Group-ACCOUNTANTS, Permissions: Read/Write
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/2f809c22-d66b-4277-b341-abdd9b63645b)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/47e23ab1-0bcf-4009-b441-a17e70f9f09b)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/c91ac43a-100e-4573-a8d8-73ec845f97d7)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/2a02246b-26fe-4092-b614-1e07a94f7afb)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/dc643112-fa76-4aab-859c-a3802c21bad5)

log in to Client-VM as bek.laxe and try to access the "not for use file" and watch it fail; then log out of Client-VM
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/cc1a6a0a-350c-41eb-96c4-f487e73acae9)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/5d18f488-249b-4c9e-a84c-399f7f984c4e)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/243b1ae8-d898-4925-9e85-768941c7ee6e)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/e3c365c8-fd41-4920-a3da-88f9939bada9)

Now go back into DC-Server and make "bek.laxe" a member of the ACCOUNTANTS security group.
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/67a15b1a-6c7e-491a-b88d-e62e57b4fe0f)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/81d4613e-09bf-47e1-b68b-23601b5a64d3)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/50304a8f-108a-4324-9ea7-754f4d49d691)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/dd057edb-25c9-40d6-8691-6cd81335945e)

Restart then log back into Client-VM as "bek.laxe", the file should be accessible 
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/e161f1c4-d369-4d29-adb4-ad4ac9deb358)
![image](https://github.com/SedinamA/Security-File-Share/assets/146953803/a48ad68c-5016-444b-b52b-bf5de0e1c04b)

Now we have a file successfully shared with the appropriate staff member of accounting.













