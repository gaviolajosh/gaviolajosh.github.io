---
  title: Proxmox Setup
  author: josh
  categories: [Homelab]
  tags: [homelab, tutorial, Proxmox VE]
---
This is the main hypervisor for my Homelab  

# **Setup Info**  
I used this [tutorial](https://www.youtube.com/watch?v=sZcOlW-DwrU) from [Craft Computing](https://www.youtube.com/@CraftComputing).



I was unable to use a RAID/ZFS configuration due to my setup limit at the time of my homelab setup. So I opted to use LVM storage.  
I plan on upgrading my storage array in the future with either former enterprise SAS HDDs or new SATA HDDs.  

My current setup is an AMD Ryzen 5 2600X, 16GB DDR4 NON-ECC RAM, 512GB Sata SSD  
![image](https://github.com/adnapJosh/homelab/assets/44041134/224e142f-ffef-4a3e-848c-6c6282570db2)  
(I promise it runs longer, I just had to move the setup so the runtime is low)

# **Backups**  
As I'm still experimenting with configurations and services I want to use, I'm constantly spinning up, editting, and removing VMs and LXCs. Therefore, I use Proxmox's automatic backup system to save up to 4 instances of backups for any one machine at a time. I have these set to backup weekly as to not lose too much progress if a backup restoration is needed.
