---
  title: Basic Networking Practice
  author: josh
  categories: [Homelab]
  tags: [networking, dhcp]
---

In my current position, there is not much work for me to practice my networking skills, so I feel as if I might lose some proficiency with Cisco's CLI and all the regular commands.
I started up my EVE-NG VM again and went to work trying out some basic router configurations, using it as a DHCP server, etc.

EVE-NG's website has some good [documentation](https://www.eve-ng.net/index.php/documentation/howtos/howto-add-cisco-dynamips-images-cisco-ios/) on getting an IOS loaded into the VM, but there's some hiccups I experienced on the way.

It can be hard to have the exact image/version that is known to be supported on EVE-NG. For instance, in the documentation on EVE=NG's website, it mentions using `c3725-adventerprisek9-mz.124-15.T14.bin` as the supported version, but I had `c3725-adventerprisek9-mz124-15.bin`. Notice the lack of `.T14` in mine. Luckily for me if you just alter file and folder names to accommodate the missing `.T14` it worked fine. 


However this isn't always the case, because in my first attempt I tried to use `c7200-adventerprisek9-mz.124-24.T5.image`, which isn't the supported `c7200-adventerprisek9-mz.152-4.S6.bin` or `c7200-adventerprisek9-mz.152-4.S2.bin` images. At the end of the day I was just glad to get one of the images working.


One more thing to note. In the documentation it mentions calculating the IDLE-PC usage in order to lower the CPU usage of the simulated router. My first router's best/highest tested IDLE-PC value was `0x61499868` but the default value was something else which would make all other routers have a higher default CPU usage. While it does say where to put the information for the node you just did it on, it does not say how to make that the default configuration.


I found this [blog](https://thecciejourney.wordpress.com/2018/04/17/eve-ng-default-idle-pc/) which said that in order to make it default, you had to go change the IDLE-PC value of the template. In my case, mine was a little different to the blod and I used:
```
nano /opt/unetlab/html/templates/intel/c3725.yml
```
Now all my future nodes will have the lowest CPU usage on the VM as tested.

![alt text](/assets/2024-10-13-dynamips.png)
