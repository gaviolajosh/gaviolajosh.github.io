---
title: Proxmox full host migration & decommission
author: josh
categories: [Homelab]
tags: [homelab, tutorial, Proxmox VE]
---

I have been working on setting up my new-to-me Dell Poweredge R720 to become my new hypervisor host, and with that comes not wanting to lose the past data from my previous hypervisor host.  
This was a fairly daunting task for me, as I wanted to make sure that I did not lose any pre-existing configs for my VMs and containers as it would add unnecessary downtime to my network.  


I decided to utilize Proxmox's restore from backup feature, as I have had previously set backups to be scheduled every weekend. 
There are other alternatives such as just moving all the drives over to the new host and hoping the system works (Linux makes this fairly easy), 
but I felt that restoring from backups would make the process a lot more stable.  
The idea to utilize an NFS or set the new host as a cluster and migrate configs that way was floated to me, but I didn't have the time or knowledge to do that correctly.   
(It is something I hope to have experience with in the future)   

I mainly followed this [tutorial](https://www.youtube.com/watch?v=E60_FC967YE) from [ElectronicsWizardry](https://www.youtube.com/@ElectronicsWizardry) to lay out my options and see how this would be done.
First I needed a temporary transferable device to save my backups to, so I used a spare 128Gb SSD to create a VZ-Dump file and Snippet directory in Proxmox. 
After all of the backups were on the SSD I was able to transfer that to the fresh install of Proxmox on the R720, mount the drive in the Proxmox shell, and create another temporary directory to load my configs from. 
Once the drive is recognized by the new host, it's as easy as hitting a button to restore the VM.

<img width="280" alt="image" src="https://github.com/user-attachments/assets/33e9fd59-f2d3-4b3e-8410-b42932309dcd">

One thing that I did encounter was that I did not carry over the ISO files for VMs initially and it brought up an error that the ISO did not exist in the expected location.

<img width="419" alt="image" src="https://github.com/user-attachments/assets/206576c9-5987-45f2-aa55-e100ea06ef83">

This is easily remedied by uploading the proper ISO and changing the location to the drive you store VMs on in this Proxmox config.

