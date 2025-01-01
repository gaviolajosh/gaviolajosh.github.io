---
title: Basic Active Directory Setup Practice
author: josh
categories: [Homelab]
tags: [homelab, AD]
---

I've been seeing a lot of job postings wanting experience in Active Directory, and since I don't have a way to gain that experience through my current job, I've decided to do the practice in my own homelab.  
To start I needed 2 things, a Windows Server ISO and a Windows Enterprise ISO. Fortunately, Windows allows you to download the OS without having to pay for a license as a trial.  


I opted to use [Windows Server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019) and [Windows 10 Enterprise LTSC](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise). 
I could have used, Windows Server 2022 and Windows 11 Enterprise, but I figured that many businesses will be late to overhaulding the OS on most of their systems for a few years. However, I should practice on those versions in the future.  

First I started with the setup of the Windows Server VM, and with that I needed to:
- name to computer
- the domain
- set a static ip
- and ensure the timezone was correct

![image](https://github.com/gaviolajosh/blog/assets/44041134/71e87ab5-c115-4cb3-a5e6-54cc9572c644)  

After that, I set the roles and features of this OS install, which the important one was Active Directory Domain Services and also the DNS Server.
Even though I have a DNS server already set up on my network, this was necessary for the Windows 10 computer to resolve the domain name.  
![image](https://github.com/gaviolajosh/blog/assets/44041134/cdcb161c-63e3-4a0a-8cc1-fbe2439f8403)

Since this is a fresh install and domain controller, I had to use the AD Domain Services Config Wizard to create a new forest and set the root domain name. (I don't have a screenshot for this, but you can access the wizard from the notification pulldown)  
![image](https://github.com/gaviolajosh/blog/assets/44041134/26d96c7d-0162-484d-a666-d631a320192d)

Next was setting up the DC Admin Account.
You can access the Users and Computers setup from the Tools pulldown in the rop right.  
![image](https://github.com/gaviolajosh/blog/assets/44041134/66811c23-e02b-4b34-b7e1-7b0d8889937c)

The UI functions very similarly to a normal Windows File Manager, and you can right click to add new objects like folder and user and such.  
![image](https://github.com/gaviolajosh/blog/assets/44041134/31aacdaf-f90b-4434-87da-08e90bca51f4)

I moved on to the Windows 10 **Enterprise** VM next. (It must be enterprise or you can't use all the AD features)  
((actually you might be able to use pro but most enterprises will use enterprise ISOs))  
Navigate to this section of the settings, and select advanced system settings.  
![image](https://github.com/gaviolajosh/blog/assets/44041134/df5ff7c9-05e1-4a3d-aec6-2149b3e7b1f3)

After that I changed the computer name and the domain to the one I set up earlier.  
![image](https://github.com/gaviolajosh/blog/assets/44041134/6cb759bc-b9fb-42d8-8ace-ca1a25697dd4)

After that this computer is now linked to the AD DC, and is can now be controlled by the DC and it's admins.  



