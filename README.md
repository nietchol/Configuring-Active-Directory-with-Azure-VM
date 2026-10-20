# Configuring-Active-Directory-with-Azure-VM
This tutorial outlines the prerequisites and installation of Active Directory Services with Azure Virtual Machines<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

-Windows Server 2022 Datacenter: Azure Edition Hotpatch
-Windows 11 Pro, version 25H2

<h2>List of Prerequisites</h2>

-Microsoft Azure account and subscription

-Credit card for subscription, required to use Azure's services.
<p></p>
<p>
<img width="959" height="440" alt="Screenshot 2026-10-05 151244" src="https://github.com/user-attachments/assets/aee660dd-9f4a-40c3-9e5d-515969507612" />
</p>
<p>
  1. Sign up for Microsoft Azure. Navigate to resource groups or search for resource groups in the search bar.
</p>
<p>
<img width="959" height="440" alt="Screenshot 2026-10-05 152147" src="https://github.com/user-attachments/assets/d0e5ff5e-97fa-490e-a9c6-70a13d938c42" />
</p>
<p>
  2. Click Create, input a name and then click "Review + create". Disregard the other options but remember the name and region.
</p>
<br />
<p>
<img width="959" height="437" alt="Screenshot 2026-10-05 152254" src="https://github.com/user-attachments/assets/286f43f4-67b6-4f0c-97bc-08ce7862ba3b" />
</p>
<p>
<img width="959" height="438" alt="Screenshot 2026-10-05 152459" src="https://github.com/user-attachments/assets/34b286be-fc28-4b39-b157-c73c9b807ab6" />
</p>
<p>
  4. Navigate to Virtual Machines (VM) or search for Virtual Machines in the search bar. On the VM page, click Create. This will be the domain controller
</p>
<p>
<img width="959" height="438" alt="Screenshot 2026-10-05 152628" src="https://github.com/user-attachments/assets/18e416f5-afdb-4d87-ac3a-9da67e9432c4" />
</p>
<p>
  6. Under Resource group, use the recently created resource group and choose a memorable name for a domain controller. Under Region, use the same region as the resource group.
</p>
<p>
<img width="959" height="437" alt="Screenshot 2026-10-05 152707" src="https://github.com/user-attachments/assets/295ad966-1336-4fc5-86ff-9a1be92c33d3" />
</p>
<p>
 For the image, select a Windows Server. Here, I select the 2022 Datacenter edition. Other versions will have slightly different features. For size, select any available processor.
</p>
<br />
<p>
<img width="956" height="408" alt="Screenshot 2026-10-05 152903" src="https://github.com/user-attachments/assets/5d79b958-af34-45a8-9919-1866db25ce9a" />
</p>
<p>
    7. Select a username and password for the Administrator account on the server.
</p>
<p>
<img width="959" height="443" alt="Screenshot 2026-10-05 153102" src="https://github.com/user-attachments/assets/bf60f4f4-db1f-47c4-8183-426eb1270748" />
</p>
<p>
   8. Allow public inbound port 3389 for remote desktop access and check the box to use an existing License. Note that the network name under the network section will be used for the client VM as well. Now click "Review + create". Other input bars and sections can be left as default or blank.
</p>
<br />
<p>
<img width="959" height="440" alt="Screenshot 2026-10-05 211156" src="https://github.com/user-attachments/assets/d138d630-5424-4044-89db-7ae7de16f07b" />
</p>
<p>
  9. After deployment is complete, navigate to Virtual Machines (VM) or search for Virtual Machines in the search bar. Click Create.
</p>
<br />
<p>
<img width="959" height="435" alt="Screenshot 2026-10-05 211529" src="https://github.com/user-attachments/assets/87566511-4b01-4e07-9251-c713ae4a4d36" />
</p>
<p>
10. For resource group and region, use the newly created resource group and its region.
</p>
<p>
  <img width="959" height="436" alt="Screenshot 2026-10-05 211547" src="https://github.com/user-attachments/assets/da565bff-c5af-4c8c-87c5-c30a66933717" />
</p>
<p>
  11. Choose a memorable name for the client VM. Select Windows 11 Pro and any available processor for the Image and size. Also choose a username/password for the Administrator account.
</p>
<p>
  <img width="958" height="436" alt="Screenshot 2026-10-05 211615" src="https://github.com/user-attachments/assets/b8b1b580-7b27-4ed0-86e2-c5dac9b19c3a" />
</p>
<p>
  12. Allow inbound port 3389 and check the box under licensing.
</p>
<p>
  <img width="959" height="438" alt="Screenshot 2026-10-05 211703" src="https://github.com/user-attachments/assets/d49c7a3c-5842-4b5e-8f6e-9a617d1cf201" />
</p>
<p>
  13. Navigate to the Networking tab and select the same virtual network and subnet as the other VM. Then click "Review + create".
</p>
<p>
  <img width="959" height="438" alt="Screenshot 2026-10-05 212412" src="https://github.com/user-attachments/assets/4124644c-b62f-49b5-8d14-a80b58618a78" />
</p>
<p>
  14. Now we need to make the private IP address remain static. Click on the Domain Controller on the VM page
</p>
<p>
  <img width="958" height="438" alt="Screenshot 2026-10-05 212713" src="https://github.com/user-attachments/assets/797f8a7c-7648-42e9-95f8-6b71a4ba4e0f" />
</p>
<p>
  15.Click on Network settings on the Navigation bar.
</p>
<p>
  <img width="955" height="440" alt="Screenshot 2026-10-05 212734" src="https://github.com/user-attachments/assets/7c8d996e-68d5-468a-bf4c-0a95f3fbb5a6" />
</p>
<p>
  16. Click on the IP Configurations link near the top.
</p>
<p>
  <img width="952" height="429" alt="Screenshot 2026-10-05 212749" src="https://github.com/user-attachments/assets/fbc63736-ee48-4530-81b3-7667973a2287" />
</p>
<p>
   17. Click on ipconfig1 link in the table. 
</p>
<p>
  <img width="959" height="440" alt="Screenshot 2026-10-05 212921" src="https://github.com/user-attachments/assets/12684dba-7d96-4a54-ab50-104b078a603b" />
</p>
<p>
  18. Click on the static bubble under Private IP address settings and click Save. We will use the Domain Controller as the client's DNS server. A server with a static, private IP address will retain the same address, so we will not have to update the client's DNS server address every time the server's address changes (as it would when restarting a server configured with dynamic IP addressing). Copy the private IP address but do not edit it.
</p>
<p>
  <img width="958" height="437" alt="Screenshot 2026-10-05 213103" src="https://github.com/user-attachments/assets/29419d4e-3674-468d-a273-cb723f39b158" />
</p>
<p>
  19. Navigate to the client's IP Configurations page and click on DNS Servers under Settings on the Navigation bar.
</p>
<p>
  <img width="958" height="436" alt="Screenshot 2026-10-05 213211" src="https://github.com/user-attachments/assets/c5412d0f-202d-4cd1-bbf2-c42f71918816" />
</p>
<p>
  20. Click the Custom bubble and paste the server's private IP address. Click Apply.
</p>
<p>
  <img width="959" height="437" alt="Screenshot 2026-10-05 213257" src="https://github.com/user-attachments/assets/27261f76-dcb2-433c-96b7-30ea0f86be82" />
</p>
<p>
  21. Navigate back to the VM page and restart the Client. Click on the client VM link and click Restart near the top.
</p>
<br />
<p>
  <img width="958" height="440" alt="Screenshot 2026-10-05 220232" src="https://github.com/user-attachments/assets/c5222abc-1145-4b29-be70-e6cbde53ec8e" />
  <p>
    22.On the VM page, copy the Domain Controller's private IP address.
  </p>
  <br />
</p>
<p>
  <img width="953" height="461" alt="Screenshot 2026-10-05 220302" src="https://github.com/user-attachments/assets/d13863ae-8f1e-46d1-97b8-4bb53514a926" />
</p>
<p>
  23.Search for Remote Desktop Connection on the Windows Start menu and run the program.
</p>
<br />
<p>
  <img width="302" height="368" alt="Screenshot 2026-10-19 142926" src="https://github.com/user-attachments/assets/698bdab1-40ef-4ce9-9ef4-f7c82c4ee7fc" />
</p>
<p>
  24. On the Remote Desktop Connection app, click on More options and paste the IP address as the Computer name. Enter the same username you used as the Administrator account for the Domain Controller. Click Connect and enter the password when prompted.
</p>
<br />
<p>
  <img width="837" height="496" alt="Screenshot 2026-10-09 171527" src="https://github.com/user-attachments/assets/30fd3b5f-ec21-42cc-bb51-8c0f53db952b" />
</p>
<p>
  25. On the Dashboard, click on Add roles and features under Configure this local server.
</p>
<p>
  <img width="833" height="496" alt="Screenshot 2026-10-09 171540" src="https://github.com/user-attachments/assets/dc3f21f2-a294-4009-9280-7e964977a700" />
</p>
<p>
  26-27. Click Next on the first 2 steps and select your server name on the Server Selection tab. Click Next.
</p>
<br />
<p>
  <img width="830" height="482" alt="Screenshot 2026-10-09 171557" src="https://github.com/user-attachments/assets/a8014d7f-600d-487e-a907-6ab714be7341" />
</p>
<p>
  <img width="361" height="256" alt="Screenshot 2026-10-09 171618" src="https://github.com/user-attachments/assets/3e79e8c3-4684-47d7-af95-bb789076383e" />
</p>
<p>
  28. Check the "Active Directory Domain Services" box and accept to install associated apps/services.
</p>
<br />
<p>
  <img width="362" height="257" alt="Screenshot 2026-10-09 171631" src="https://github.com/user-attachments/assets/72d0a851-d697-4aa3-a1de-a2592f40a539" />
</p>
<p>
  <img width="362" height="257" alt="Screenshot 2026-10-09 171640" src="https://github.com/user-attachments/assets/c3a80ea7-7b9c-401b-84ae-ffda495c5757" />
</p>
<p>
  <img width="361" height="258" alt="Screenshot 2026-10-09 171650" src="https://github.com/user-attachments/assets/780dd917-1891-4283-b88e-8a121252c10b" />
</p>
<p>
  29-31. Click Next until the Confirmation tab, then click Install.
</p>
<br />
<p>
  <img width="833" height="475" alt="Screenshot 2026-10-09 092256" src="https://github.com/user-attachments/assets/0d9b8cb5-4a84-4ac4-a7e7-8b5ab38cb222" />
</p>
<p>
  32. Hover/click on the yellow flag in the top-right corner and click "Promote this server to a domain"
</p>
<br />
<p>
  <img width="350" height="256" alt="Screenshot 2026-10-09 092452" src="https://github.com/user-attachments/assets/396410f9-5c5f-40fb-aeed-3d57e8f6f1d2" />
</p>
<p>
  33. Click on the bubble "Add a new forest" and enter any domain name which must end with ".com", e.g., mydomain.com. Click Next.
</p>
<p>
  <img width="350" height="254" alt="Screenshot 2026-10-09 092510" src="https://github.com/user-attachments/assets/0b31ba4c-80c8-4c89-bab0-c78f91f0757d" />
</p>
<p>
  34. Enter a password for the Directory Services Restore Mode. Ignore other options. Click Next.
</p>
<p>
  <img width="353" height="259" alt="Screenshot 2026-10-09 092531" src="https://github.com/user-attachments/assets/e755b178-9e1c-48d1-b3cc-3b19d4de805f" />
</p>
<p>
  35. Leave the "Create DNS Delegation" box unchecked and click Next
</p>
<p>
  <img width="702" height="421" alt="Screenshot 2026-10-09 092618" src="https://github.com/user-attachments/assets/1cec58b4-b229-4f6d-be75-492d7db495f9" />
</p>
<p>
  36. Click Next until the Installation tab and click Install. The server will restart.
</p>
<p>
  <img width="303" height="368" alt="Screenshot 2026-10-09 094136" src="https://github.com/user-attachments/assets/65e4fa2e-4c16-458f-a8ed-b32227ed5273" />
</p>
<p>
  <img width="552" height="428" alt="Screenshot 2026-10-09 100215" src="https://github.com/user-attachments/assets/ae953daa-ea25-4b0e-a6b0-db644bf69964" />
</p>
<p>
  <img width="156" height="200" alt="Screenshot 2026-10-09 100617" src="https://github.com/user-attachments/assets/13c3ddda-5532-4092-848d-ffb333a7d6d2" />
</p>
<p>
  <img width="555" height="428" alt="Screenshot 2026-10-09 101024" src="https://github.com/user-attachments/assets/1a30ae7a-3987-4a0e-aaa1-a4897b7b9fcc" />
</p>
<p>
<img width="899" height="491" alt="Screenshot 2026-10-09 101832" src="https://github.com/user-attachments/assets/7fb32bbc-f1ea-4592-814a-4118d3205df4" />
</p>
