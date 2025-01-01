---
title:  2-node Proxmox cluster w/o HA
author: josh
categories: [Homelab]
tags: [homelab, '7010']
---
In my last post, I mentioned that utilizing an R720 24/7 for my mission critical services was:
1. Being far too underutilized
2. Pulling more watts when idle than I'd like

I really needed it just for VMs or configurations that used more resources than I had at the time, such as [Eve-NG](https://gaviolajosh.github.io/blog/eve-ng/).
Making another Proxmox host seemed to be my best bet in separating what's 24/7 necessary and what isn't. I wanted something power efficient, 
small enough to fit in a rack shelf, and with enough headroom for more services down the line. I landed on a Dell Optiplex 7010 DT. (Not the new one from 2024) 
((Very dumb decision from Dell to reuse the name))


The specs on this Optiplex is:
- Core i7 3770 4c/8t 3.4GHz
- 16Gb DDR3 1600MHz RAM
  - The manual says it only supports 16Gb, but online I've seen some people have success with running 32Gb total
- 2 x 256Gb Sata SSD running in Raid 0

While managing 2 separate Proxmox installs would have been easy because it's only 2 hosts, 
I wanted to learn about node clustering because I tend to see that being used at the datacenter.
Proxmox itself generally only likes having 3-node clustering to maintain quorum between the nodes. 
Which before this I didn't know quorum was a thing, let alone maintaing it to avoid split-brain between nodes. 
It was definitely a learning experience to understand how clustering servers worked, and I haven't even done it "correctly". 

Will write the rest later.
