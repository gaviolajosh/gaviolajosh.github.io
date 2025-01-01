---
title: Future Plans (CEPH, (HA?) clustering)
author: josh
categories: [Homelab]
tags: [homelab]
---

As great as having a powerful R720 as my hypervisor host, I think I've hit the point where it's too much to have on 24/7.


I was able to get my idle power to around 98W which is very respectable and not too bad for the cost of electricity where I live, 
but I think the extra compute is creating an unnecessary cost for the long term. 
My tasks that I have running almsot 100% of the time really don't take that much compute, so I'm thinking that I should redo my my setup. 
Ideally I would have a cluster where my main/everyday host is a system with a much smaller footprint and the R720 can become my sandbox for testing. 
That way I can mitigate average running costs and just utilize the R720 whenever I really need to test/work in a VM (like EVE-NG).

Because I work in a datacenter, I've been able to get a better idea of eneterprise standards for redundancy such as HA clusters. 
(Right now) I don't think I would ever get to the point where I would need something like a 3-node cluster to have it up 99.99% of the time, but it's a good idea to mess with. 
I also think that because I am going to be using a cluster for a smaller system, I should use CEPH where all the storage is accessible 100% of the time on the main host. 
That way I don't have to worry about needed to power up the R720 just for some data transfer.
