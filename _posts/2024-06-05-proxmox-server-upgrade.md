---
title:   Proxmox Server CPU Upgrade
author: josh
categories: [Homelab]
tags: [homelab]
---
I was able to upgrade the CPU of my Proxmox host from a Ryzen 5 2600x (6c/12t) to a Ryzen 7 3700x (8c/16t).
While the swap was not entirely necessary, I appreciate having the extra breathing room for my CPU usage which will allow me to utilize more CPU intensive VMs and services in the future.  



Some other aspects of this upgrade that are notable are:
- Zen 1 -> Zen 2 architecture
- 2933 MT/s -> 3200 MT/s for higher RAM speed
- 95W TDP -> 65W TDP for lower idle power usage
- PCI-E Gen 3 -> Gen 4 for hardware compatability down the road

I'll most likely use the 2600x for a future standalone NAS build, but for now the next upgrade plans are higher capacity RAM or more storage to run ZFS to store VM backups.
