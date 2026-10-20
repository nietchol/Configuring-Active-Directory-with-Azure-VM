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
<p>
<img width="959" height="440" alt="Screenshot 2026-10-05 151244" src="https://github.com/user-attachments/assets/aee660dd-9f4a-40c3-9e5d-515969507612" />
</p>
<p>
<img width="959" height="440" alt="Screenshot 2026-10-05 152147" src="https://github.com/user-attachments/assets/d0e5ff5e-97fa-490e-a9c6-70a13d938c42" />
</p>
<p>
<img width="959" height="437" alt="Screenshot 2026-10-05 152254" src="https://github.com/user-attachments/assets/286f43f4-67b6-4f0c-97bc-08ce7862ba3b" />
</p>
<p>
<img width="959" height="438" alt="Screenshot 2026-10-05 152459" src="https://github.com/user-attachments/assets/34b286be-fc28-4b39-b157-c73c9b807ab6" />
</p>
<p>
<img width="959" height="438" alt="Screenshot 2026-10-05 152628" src="https://github.com/user-attachments/assets/18e416f5-afdb-4d87-ac3a-9da67e9432c4" />
</p>
<p>
<img width="959" height="437" alt="Screenshot 2026-10-05 152707" src="https://github.com/user-attachments/assets/295ad966-1336-4fc5-86ff-9a1be92c33d3" />
</p>
<p>
<img width="956" height="408" alt="Screenshot 2026-10-05 152903" src="https://github.com/user-attachments/assets/5d79b958-af34-45a8-9919-1866db25ce9a" />
</p>
<p>
<img width="959" height="443" alt="Screenshot 2026-10-05 153102" src="https://github.com/user-attachments/assets/bf60f4f4-db1f-47c4-8183-426eb1270748" />
</p>
<p>
<img width="959" height="440" alt="Screenshot 2026-10-05 211156" src="https://github.com/user-attachments/assets/d138d630-5424-4044-89db-7ae7de16f07b" />
</p>
<p>
<img width="959" height="435" alt="Screenshot 2026-10-05 211529" src="https://github.com/user-attachments/assets/87566511-4b01-4e07-9251-c713ae4a4d36" />
</p>
<p>
  <img width="959" height="436" alt="Screenshot 2026-10-05 211547" src="https://github.com/user-attachments/assets/da565bff-c5af-4c8c-87c5-c30a66933717" />
</p>
<p>
  <img width="958" height="436" alt="Screenshot 2026-10-05 211615" src="https://github.com/user-attachments/assets/b8b1b580-7b27-4ed0-86e2-c5dac9b19c3a" />
</p>
<p>
  <img width="959" height="438" alt="Screenshot 2026-10-05 211703" src="https://github.com/user-attachments/assets/d49c7a3c-5842-4b5e-8f6e-9a617d1cf201" />
</p>
<p>
  <img width="959" height="438" alt="Screenshot 2026-10-05 212412" src="https://github.com/user-attachments/assets/4124644c-b62f-49b5-8d14-a80b58618a78" />
</p>
<p>
  <img width="958" height="438" alt="Screenshot 2026-10-05 212713" src="https://github.com/user-attachments/assets/797f8a7c-7648-42e9-95f8-6b71a4ba4e0f" />
</p>
<p>
  <img width="955" height="440" alt="Screenshot 2026-10-05 212734" src="https://github.com/user-attachments/assets/7c8d996e-68d5-468a-bf4c-0a95f3fbb5a6" />
</p>
<p>
  <img width="952" height="429" alt="Screenshot 2026-10-05 212749" src="https://github.com/user-attachments/assets/fbc63736-ee48-4530-81b3-7667973a2287" />
</p>
<p>
  <img width="959" height="440" alt="Screenshot 2026-10-05 212921" src="https://github.com/user-attachments/assets/12684dba-7d96-4a54-ab50-104b078a603b" />
</p>
<p>
  <img width="958" height="437" alt="Screenshot 2026-10-05 213103" src="https://github.com/user-attachments/assets/29419d4e-3674-468d-a273-cb723f39b158" />
</p>
<p>
  <img width="958" height="436" alt="Screenshot 2026-10-05 213211" src="https://github.com/user-attachments/assets/c5412d0f-202d-4cd1-bbf2-c42f71918816" />
</p>
<p>
  <img width="959" height="437" alt="Screenshot 2026-10-05 213257" src="https://github.com/user-attachments/assets/27261f76-dcb2-433c-96b7-30ea0f86be82" />
</p>
<p>
  <img width="958" height="440" alt="Screenshot 2026-10-05 220232" src="https://github.com/user-attachments/assets/c5222abc-1145-4b29-be70-e6cbde53ec8e" />
</p>
<p>
  <img width="953" height="461" alt="Screenshot 2026-10-05 220302" src="https://github.com/user-attachments/assets/d13863ae-8f1e-46d1-97b8-4bb53514a926" />
</p>
<p>
  <img width="302" height="368" alt="Screenshot 2026-10-19 142926" src="https://github.com/user-attachments/assets/698bdab1-40ef-4ce9-9ef4-f7c82c4ee7fc" />
</p>
<p>
  <img width="837" height="496" alt="Screenshot 2026-10-09 171527" src="https://github.com/user-attachments/assets/30fd3b5f-ec21-42cc-bb51-8c0f53db952b" />
</p>
<p>
  <img width="833" height="496" alt="Screenshot 2026-10-09 171540" src="https://github.com/user-attachments/assets/dc3f21f2-a294-4009-9280-7e964977a700" />
</p>
<p>
  <img width="830" height="482" alt="Screenshot 2026-10-09 171557" src="https://github.com/user-attachments/assets/a8014d7f-600d-487e-a907-6ab714be7341" />
</p>
<p>
  <img width="361" height="256" alt="Screenshot 2026-10-09 171618" src="https://github.com/user-attachments/assets/3e79e8c3-4684-47d7-af95-bb789076383e" />
</p>
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
  <img width="895" height="488" alt="Screenshot 2026-10-09 092239" src="https://github.com/user-attachments/assets/a2920d50-e071-4db5-8b93-7fd26c783c61" />
</p>
<p>
  <img width="833" height="475" alt="Screenshot 2026-10-09 092256" src="https://github.com/user-attachments/assets/0d9b8cb5-4a84-4ac4-a7e7-8b5ab38cb222" />
</p>
<p>
  <img width="350" height="256" alt="Screenshot 2026-10-09 092452" src="https://github.com/user-attachments/assets/396410f9-5c5f-40fb-aeed-3d57e8f6f1d2" />
</p>
<p>
  <img width="350" height="254" alt="Screenshot 2026-10-09 092510" src="https://github.com/user-attachments/assets/0b31ba4c-80c8-4c89-bab0-c78f91f0757d" />
</p>
<p>
  <img width="353" height="259" alt="Screenshot 2026-10-09 092531" src="https://github.com/user-attachments/assets/e755b178-9e1c-48d1-b3cc-3b19d4de805f" />
</p>
<p>
  <img width="702" height="421" alt="Screenshot 2026-10-09 092618" src="https://github.com/user-attachments/assets/1cec58b4-b229-4f6d-be75-492d7db495f9" />
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
