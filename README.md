# 🎉Active-Directory-Lab 

## Objective

Simulated a real-world helpdesk environment by deploying a Windows Server-based Active Directory domain, provisioning users and organizational units, configuring Group Policy for mapped network drives, and applying NTFS/share permissions to control access. The project demonstrates user onboarding processes and how to ensure secure, automated access to department resources through Group Policy. Validated configuration by logging in with domain users and confirming mapped drive functionality.

### Skills Learned

- Network Topology
- Virtualisation Setup
- Active Directory Domain Services
- Client Server Domain Integration
- File Sharing and NTFS Permissions
- Trouble Shooting and Validation 
- Statically assigning Ip Addresses 
- Creating Domain users
- Organisational Units and Groups
- Group Policy Object Enforcing 
- Mapping Network Drives

### Tools Used

- Windows Server 2022
- Active Directory 
- PowerShell
- Virtual Machines
- Snapshots
- CMD

## Steps

## *1: Network Topology Overview*

As a best practice, I’ve created a custom network diagram using draw.io to provide a clearer view of the network flow, which will help simplify troubleshooting

<img width="494" height="361" alt="image" src="https://github.com/user-attachments/assets/473655eb-8668-406e-9a43-382be655d630"/>


## *2: Virtual Machine Setup*

Before installing the virtual machines, I navigate to the Network Settings and configure them to use the NAT Network, as internal communication is required. I then proceed with the installation of the virtual machines for this project.
Network
<img width="500" height="193" alt="image" src="https://github.com/user-attachments/assets/3ed9587e-a456-45f0-9323-126a2d3685d6" />

- Server

<img src="https://github.com/user-attachments/assets/e948a1ed-f6dc-4bd5-9fea-8142e33107cc" width="380" height="285" />

- Windows 10 Pro

<img src="https://github.com/user-attachments/assets/e2ef4984-bfb6-4883-a9cf-795bb5be0b6c" width="370" height="282" />



## *3: Creating Snapshots for Rollback*

After successfully installing the virtual machines and configuring the server, I create snapshots of both systems. This serves as a rollback point in case of misconfiguration or other issues during the setup process.

<img src="https://github.com/user-attachments/assets/f6d934fe-3574-4324-90c4-97d56417a7c8" width="400" height="546" />

<img src="https://github.com/user-attachments/assets/505b05ff-af88-453c-a490-e445541d1d72" width="400" height="450" />



## *4: Renaming Machines Prior to Domain Configuration*
Before promoting the server to a domain controller, I rename the machine. This step helps prevent potential trust relationship issues and simplifies identification within the domain environment.

<img width="400" height="543" alt="image" src="https://github.com/user-attachments/assets/d0d26b0c-4d13-4b7d-84df-b7d9c474b145" />


## *5: Assigning Static IP Addresses*

To ensure network stability, consistency, and ease of management, I assign static IP addresses to all virtual machines. This avoids reliance on DHCP, which can introduce changes to IP assignments. I also configure DNS resolution to point to the domain controller, as it is hosting the DNS service. Connectivity between machines is tested to confirm proper communication

- Server

<img width="400" height="346" alt="image" src="https://github.com/user-attachments/assets/c28c7ba3-32fe-428d-a45f-d3c8135a80eb" />

- Windows Machine

<img width="400" height="347" alt="image" src="https://github.com/user-attachments/assets/e13b4834-2c89-4ca9-833d-611a8c0eca15" />

- Connectivity 

<img width="400" height="373" alt="image" src="https://github.com/user-attachments/assets/1f285c74-e95e-4ee9-9bf9-79f57aee5186" />



## *6: Configuring Server as a Domain Controller*
Next, I configure the server to act as the Domain Controller for this environment. During the setup, I select Active Directory Domain Services as the primary server role and include Certificate Services as needed. The server is then promoted to a domain controller using project-specific settings. 

<img width="400" height="536" alt="image" src="https://github.com/user-attachments/assets/b19896a7-5f15-4660-a1e4-1067403eedd0" />

<img width="400" height="534" alt="image" src="https://github.com/user-attachments/assets/8919a05a-dc72-4cbb-96e6-a3ddcc7bf10f" />

<img width="400" height="544" alt="image" src="https://github.com/user-attachments/assets/61d7c27a-195b-44eb-8b52-3a1562328a43" />




## *7: Creating Organizational Units and User Accounts*
Once the domain controller is operational, I begin organising the directory structure by creating Organizational Units and domain users. I move built-in groups into appropriate OUs to improve directory organization and management.

<img width="400" height="523" alt="image" src="https://github.com/user-attachments/assets/040c2ee6-8b0e-45e4-a364-68967447a037" />

<img width="400" height="518" alt="image" src="https://github.com/user-attachments/assets/2ecdf8ad-35f4-4332-be62-2e7aeea378c7" />

<img width="400" height="525" alt="image" src="https://github.com/user-attachments/assets/1322acc5-5bdd-423d-82c2-101dd80de56a" />

<img width="400" height="524" alt="image" src="https://github.com/user-attachments/assets/4c1e554c-445b-4d05-b7ea-cb4979a76221" />





## *8: Joining the Windows 10 Client to the Domain*

I then join the Windows 10 client machine to the domain, following the process shown in the provided screenshots. The domain join is completed successfully.

- Joining
<img width="400" height="537" alt="image" src="https://github.com/user-attachments/assets/f189ce34-d481-4038-bbd7-cf92c6e19b27" />

- Login
<img width="400" height="557" alt="image" src="https://github.com/user-attachments/assets/4f84ffcc-06f9-461d-a413-a55af67f5bb8" />


## *9: Network Drive Mapping, OU and Group Creation*
Following the domain join, I map a network drive, create additional OUs and security groups, and align them with specific shared folders. These configurations reflect the desired organizational structure.

- Security Group

<img width="400" height="543" alt="image" src="https://github.com/user-attachments/assets/130ee176-910b-402c-8173-dbf6077b56e9" />

<img width="400" height="511" alt="image" src="https://github.com/user-attachments/assets/b3bfd51f-c498-40a7-9af5-67fcf7fec08f" />

- New Share
 
<img width="400" height="520" alt="image" src="https://github.com/user-attachments/assets/dee1ab38-4e59-459a-a40a-2d0f8d7a14cf" />

- Permissions

<img width="400" height="543" alt="image" src="https://github.com/user-attachments/assets/c22b57aa-eb71-48ae-b118-be2659b31ddc" />

<img width="400" height="534" alt="image" src="https://github.com/user-attachments/assets/d7d0136d-9fb8-4f5f-b276-847baf78b54c" />


- Mapping

<img width="400" height="539" alt="image" src="https://github.com/user-attachments/assets/a8427495-e0df-4f27-9fa5-60606b137e0e" />

<img width="400" height="358" alt="image" src="https://github.com/user-attachments/assets/96a9d34b-ea3f-4489-ba27-1591365631e4" />

- Restricted Access to Network drive
<img width="400" height="539" alt="image" src="https://github.com/user-attachments/assets/04a553fa-d540-46ab-a33a-bc98c1c535eb" />

## *10: Group Policy Enforcement* 
Apply a Group Policy Object to enforce a desktop background for the Sales Department OU.

<img width="400" height="522" alt="image" src="https://github.com/user-attachments/assets/d0a35681-7dde-497f-8b75-df2242ab8ece" />

<img width="400" height="560" alt="image" src="https://github.com/user-attachments/assets/48bc9e0e-eeb2-4864-9333-f1b55e2e076f" />

<img width="400" height="532" alt="image" src="https://github.com/user-attachments/assets/d49177c9-40ba-4973-bdac-1c0984502cb0" />























