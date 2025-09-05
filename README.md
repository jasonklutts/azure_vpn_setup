

# VPN - Prerequisites and Installation

This tutorial outlines the prerequisites and installation of using a VPN.

---

## Environments and Technologies Used
- A VPN (**Proton VPN**)  
- Microsoft Azure (Virtual Machines / Compute)  
- Remote Desktop  
- Internet Information Services (IIS)  

---

## Operating Systems Used
- Windows 10 (21H2)  

---

## Steps Included
1. STEP 1 - Locate Local IP  
2. STEP 2 - Setting Up VM Using Azure  
3. STEP 3 - Locating IP Through VM (France)  
4. STEP 4 - Connecting to VPN Through VM  
5. STEP 5 - Locating IP Through VPN (Japan)  

---

## 📝 Installation Steps

### STEP 1 - Locate Local IP
Locate your own personal IP address by visiting:  
 [https://www.whatismyipaddress.com](https://www.whatismyipaddress.com)  

This site will show your local IP address. We will use this later.  
<img width="1150" height="470" alt="image" src="https://github.com/user-attachments/assets/89a7b93c-8b5e-4efb-afda-1f0020d17391" />


---

### STEP 2 - Setting Up VM Using Azure
Go to  [https://portal.azure.com](https://portal.azure.com)  
(Create a free account with $200 credit if needed).  

See **Example 2A** looking at the Virtual Machine setup page.  

**EXAMPLE 2A**  
Create the Virtual Machine named **VM-France** and select the **France Central** region. 
<img width="537" height="722" alt="image" src="https://github.com/user-attachments/assets/3b46d8d1-f2d1-41ef-9433-74636e169efb" />
 

**EXAMPLE 2B** 
Create your own Username and Password (record them for later). 
<img width="524" height="277" alt="image" src="https://github.com/user-attachments/assets/ef4cf373-ed5c-4e88-acb6-00fd72700077" />
 

**EXAMPLE 2C**  
On the “Networking” tab, match the inputs shown below:  
<img width="391" height="548" alt="image" src="https://github.com/user-attachments/assets/e9bf2ff6-8fff-4d22-8e94-9658b54d1df7" />

**EXAMPLE 2D**  
Click **Review and Create**. Once validation passes, select **Create**.  
<img width="430" height="62" alt="image" src="https://github.com/user-attachments/assets/030a9d15-02f4-48c1-84ef-86b88031d51e" />

After deployment, the VM IP is: **20.199.82.110**
<img width="1067" height="477" alt="image" src="https://github.com/user-attachments/assets/1acba2b7-7065-440e-bb2a-b54b6fe511e8" />

---

### STEP 3 – Locating IP Through VM (France)
Log into the VM using **Remote Desktop Connection**.  

**EXAMPLE 3A**  
Input the VM IP (from Example 2E) and credentials.  
<img width="398" height="478" alt="image" src="https://github.com/user-attachments/assets/30b36ecf-38a1-43fb-aa29-7b8f12d903c8" />


**EXAMPLE 3B**  
Once logged in, open a browser inside the VM and visit:  
[https://www.whatismyipaddress.com](https://www.whatismyipaddress.com)  
This shows the VM location as **France**.
<img width="1196" height="530" alt="Capture" src="https://github.com/user-attachments/assets/b2305a33-a800-4b46-bf82-d623c05cc604" />


---

### STEP 4 – Connecting to VPN (Free Version)
On your **local computer**, go to [https://protonvpn.com](https://protonvpn.com)  
Create a free account.  
Copy the Proton VPN URL (Example 4A) and paste it in the VM browser.  

**EXAMPLE 4A**  
Download and install Proton VPN on the VM. Log in with the same free account credentials.  
<img width="597" height="599" alt="Capture 1" src="https://github.com/user-attachments/assets/2961b07e-9b48-41fc-81f9-c3f42824cd5f" />


**EXAMPLE 4B**  
On the left-hand side of Proton VPN, select a country. Here we connect to **Japan**.  
<img width="1600" height="820" alt="image" src="https://github.com/user-attachments/assets/e699b7fa-a1d4-4301-a1ce-5976f9640978" />

**EXAMPLE 4C**  
Verify again at [https://www.whatismyipaddress.com](https://www.whatismyipaddress.com).  
Now the VPN shows a **Japan IP address**.  
<img width="1199" height="481" alt="Capture 2" src="https://github.com/user-attachments/assets/45442128-e691-4f9a-a6c7-beebb5d4dcd2" />

---

## 🌍 Final Results
From this exercise, we see 3 different IP addresses used to connect to the internet:  

- **Home IP (USA):** `98.178.206.33`  
- **Virtual Machine IP (France):** `20.199.82.110`  
- **Virtual Machine IP via VPN (Japan):** `149.88.103.54`  

---

## ⚠Cleanup
If you no longer need the VM, delete it from your Azure account to avoid unwanted charges.


