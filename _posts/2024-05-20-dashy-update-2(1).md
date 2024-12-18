---
title: Dashy/Docker update 2
author: josh
categories: [Homelab]
tags: [homelab, dashy]
---
So I found out that with Portainer a lot of the data is located within the portainer_data, but I haven't been able to `cd` into some of the folders inside portainer_data.  




I didn't realize the importance of user priviledge since for the most part, I could solve everything by using sudo in front of the command if access was denied.  
I found this post on [askUbuntu](https://askubuntu.com/questions/578514/no-such-file-or-directory-when-chown-on-newly-created-directory) that had a similar problem to mine and in which they used the `chown` command to give access to the $USER.  

I used a slightly modified version of the command from that post to give access and `ls` for the files in the folder, but I didn't find what I needed.  

![image](https://github.com/adnapJosh/blog/assets/44041134/b9552d76-55e5-48c3-b76b-1eed1833e40c)  

The search for my Dashy config continues!  
*and yes I'm now aware I misspelled portainer-data, but I'll change that at some point™*  
