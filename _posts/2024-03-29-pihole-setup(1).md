---
title:   Pihole & Unbound Setup
author: josh
categories: [Homelab]
tags: [homelab, tutorial, pihole]
---

In a lot of videos about homelabs, I've seen [PiHole](https://pi-hole.net/) be mentioned in almost all of them. It's a self-hosted DNS server which can block certain domains from entering your network (which a lot of times people use for ad blocking).  



I used this [video](https://www.youtube.com/watch?v=FnFtWsZ8IP0) from [Craft Computing](https://www.youtube.com/@CraftComputing) as my main walkthrough on the setup, but PiHole setup is very well documented on the [PiHole GitHub](https://github.com/pi-hole/pi-hole/#one-step-automated-install).  

```
curl -sSL https://install.pi-hole.net | bash
```  
Is the one-line command to install and run the setup.  

That video also mentions using [unbound](https://github.com/NLnetLabs/unbound) to turn PiHole into a recursive DNS server.  
The install is very easy and PiHole has [documentation](https://docs.pi-hole.net/guides/dns/unbound/?h=unbound) specifically on this usecase  

```
sudo apt install unbound
```

I chose to host mine virtualized on my Proxmox server using these configurations:  
![image](https://github.com/gaviolajosh/blog/assets/44041134/38b600d8-2387-4444-ad17-6b97a6453c20)  

PiHole is not very intensive on hardware, but I think I will allocate more RAM in the future so that it can have some extra wiggle room if the network is in high-demand.  

