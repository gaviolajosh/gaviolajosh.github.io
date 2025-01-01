---
title: Proxmox cluster update
author: josh
categories: [Homelab]
tags: [homelab, R720, "7010"]
---

# Let this be a warning when buying second-hand gear because the stability might not be all the way there anymore. 

That failed spectacularly!   
The Optiplex 7010 caught fire!

The actual clustering configuration itself was perfect. 
I was able to get a stable 2-node cluster while maintaining quorum towards the main node. 
This allowed me to separate my 24/7 mission critical services between my testing/sandbox services that I only needed sometimes, which was exactly what I wanted. 
I just didn't factor in the 7010's PSU failing and catching fire is all.



Luckily I was home at the time, and it was just a component of the motherboard catching fire when I caught it, but that could have been catastrophic. 

# Now on to how I fixed it.
I had ample backups stored on the R720 and that were created from when it was my main node and that really saved me. 
But first, I had a barely operating cluster with no quorum to be able to change any configurations via the R720. 
After some googling of people who didn't have my exact issue (I wonder why), I found out that you can kind of trick Proxmox into thinking the cluster doesn't exist. 
In the R720's CLI, if you type:
```
pvecm delnode XXX
```
you would be met with a no quorum error, but if you change what Proxmox believes is necessary for quorum/the nodes available you can regain quorum over your single node without needing to reinstall. 

For my case, I used 
```
pvecm expected 1
```
which made Proxmox now believe that there was only 1 node (the R720) in the cluster. Now this wiped the configuration from the 7010, but since that system is now unusable, I'm not too worried. 

I'm hoping to be able to reuse a majority of the hardware from the old system like CPU, RAM, SSDs, etc. but I need to test if those are still usable. 



