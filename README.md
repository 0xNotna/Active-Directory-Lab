# 🎉Active-Directory-Lab 

## Objective

Simulated a real-world helpdesk environment by deploying a Windows Server-based Active Directory domain, provisioning users and organizational units, configuring Group Policy for mapped network drives, and applying NTFS/share permissions to control access. The project demonstrates user onboarding processes and how to ensure secure, automated access to department resources through Group Policy. Validated configuration by logging in with domain users and confirming mapped drive functionality.

### Skills Learned

- Network Topology
- Statically assigning Ip Addresses 
- Creating Domain users
- Organisational Units and Groups
- Group Policy Objects 
- Ressetting Active Directory Passwords
- Enforcing GPOs
- Mapping Network Drives

### Tools Used

- Windows Server 2022
- Active Directory 
- CMD
- Virtual Machines
- Snapshots 

## Steps

## *1: Network Topology Overview*

Diagram showing the test domain environment setup including server and client VM Making it easier to troubleshoot.

<img width="601" height="480" alt="image" src="https://github.com/user-attachments/assets/dfe2be43-e88c-4f01-921e-c008c5dead82" />

## *2: VM Deployment*

Creating VMs for AD Domain Controller and Windows 10 client 

<img width="416" height="343" alt="image" src="https://github.com/user-attachments/assets/1650b605-ae73-46ca-805e-88e41db28d83" />
<img width="540" height="287" alt="image" src="https://github.com/user-attachments/assets/d7e99f8f-21e9-4e0a-9378-a33f8f6cd6b1" />

## *3: Installing and Configuring Active Directory Domain Servicesl*

This is where I learned the steps involved in setting up and managing a domain controller.

<img width="465" height="323" alt="image" src="https://github.com/user-attachments/assets/f314045b-ef48-4367-a4fd-5962c3902cfc" />
<img width="465" height="323" alt="image" src="https://github.com/user-attachments/assets/60c6ca15-45b0-4450-9393-9cb0bae4a254" />

## *4: Static IP Assignment*
Ensures reliable DNS/domain resolution in lab environment

<img width="385" height="301" alt="image" src="https://github.com/user-attachments/assets/3574a35d-5a81-4570-8532-29ba2e794c93" />

## *5: Testing Domain Connectivity VIA Ping*

Validated network communication between client and server

<img width="452" height="198" alt="image" src="https://github.com/user-attachments/assets/b437492d-e935-470c-bdb5-06556e20501b" />

## *6: Joining Windows 10 Client to Domain*
Connected Windows machine successfully to domain 

<img width="416" height="343" alt="image" src="https://github.com/user-attachments/assets/d31be799-8e6b-441c-885d-c9f0d63b3a6f" />

## *7: Creating User Accounts and Organizing OUs*
Simulated department-based structure using OUs

<img width="416" height="343" alt="image" src="https://github.com/user-attachments/assets/c03cf749-f368-4eb6-b3aa-093f9aa11e9e" />

## *8: Creating and Mapping Shared Drive with NTFS Permissions *

Configured access control for department files via shared folder and GPO.

<img width="416" height="343" alt="image" src="https://github.com/user-attachments/assets/c01da43f-8faf-4d27-838f-51bb67cb08ef" />
<img width="416" height="343" alt="image" src="https://github.com/user-attachments/assets/58f57a9b-a30c-4b87-b08a-2d08a38c2d74" />
<img width="416" height="343" alt="image" src="https://github.com/user-attachments/assets/cca8e42c-599f-47a5-9ace-daab81863e57" />

## *8: GPO *

Succuessfully Applied a GPO

<img width="963" height="706" alt="image" src="https://github.com/user-attachments/assets/dc18f138-216a-4c06-9d09-e6c01efd9e79" />











