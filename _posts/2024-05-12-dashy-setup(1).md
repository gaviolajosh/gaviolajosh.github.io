---
title:  "Dashy setup"
author: josh
categories: [Homelab]
tags: [homelab, tutorial, dashy]
---
[Dashy](https://dashy.to/) has a very easy setup process with Docker which they have on the website's [quick start](https://dashy.to/docs/quick-start) guide.  



```
docker run -d \
  -p 8080:8080 \
  -v ~/my-conf.yml:/app/user-data/conf.yml \
  --name my-dashboard \
  --restart=always \
  lissy93/dashy:latest
```  
After the intialization, the Dashy dashboard is accessed through `http://localhost:8080`  

I was able to put most of the services that have a web-gui through Dashy's interactive editor instead of the config file, which is a nice touch.  
![image](https://github.com/adnapJosh/homelab/assets/44041134/df03a449-7340-484d-8520-aa04c685a5b8)

Once I get more services up and running, I'm sure that my dashboard items will expand.
