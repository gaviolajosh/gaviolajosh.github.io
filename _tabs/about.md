---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

Hello my name is Josh, and here I'll be posting update on the various projects and homelab technologies I'm working with.  
This site is hosted using [GitHub Pages][github-pages] using a template of the [Chirpy][chirpy] theme.  

My current homelab as of 1/1/2025 is:

Rack: 
* Rosewill 25U 4 post adjustable rack

Servers:
* Dell R720
  * CPU: 1x 10-Core Intel Xeon E5-2680V2 @ 2.8GHz
  * RAM: 96GB DDR3 ECC @ 1600MHz
  * Storage:
    * 2x 256GB SATA SSD (RAID1 &#124; OS & Backup 1) 
    * 2x 4TB SATA HDD (RAID1 &#124; VMs, IOSes, Backup 2)
  * OS: [Proxmox VE][proxmox]
  * Lab Environments:
    * [Active Directory][ad]
    * [Eve-NG][eve-ng]
  * Services:
    * [WireGuard][wireguard]
    * [Docker][docker]:
      * [Portainer][portainer]:
        * [Dashy][dashy]
        * [DuckDNS][duckdns]
        * [NGINX][nginx]
        * [Glances][glances]
    * [PiHole][pihole]

Networking:  
* 2x Cisco Catayst 3850 48P for testing
* Cisco SG300-10 10p switch
* TP-Link tl-sg105e 5p switch
* TP-Link POE injector
* TP-Link EAP223

Power:
* APC ES 650 UPS
* Tripplite 120V 5-15 PDU
  
# Future Plans
- [ ] Create a network diagram to easily display what services and systems I use
- [ ] Potentially move towards more recent, lower powered servers and keep the R720 only for testing purposes
- [ ] Learn more about [Ansible](https://www.ansible.com/) and [Terraform](https://www.terraform.io/) and see if deploying them would be useful
  - [ ] Learn YAML  
- [ ] Potentially move away from 3rd party cloud based security and utilize self-hosted security and storage management
- [ ] Create a NAS
- [ ] Locally create SSL certificates
- [ ] Get a standalone PFsense/OpenWRT/OPNsense device

[github-pages]: https://pages.github.com/
[jekyll]:       https://jekyllthemes.org/
[pihole]:       https://gaviolajosh.github.io/pihole-setup/
[wireguard]:    https://gaviolajosh.github.io/wireguard-setup/
[dashy]:        https://gaviolajosh.github.io/dashy-setup/
[llama3]:       https://ollama.com/
[eve-ng]:       https://gaviolajosh.github.io/eve-ng/
[portainer]:    https://www.portainer.io/
[duckdns]:      https://www.duckdns.org/
[ad]:           https://gaviolajosh.github.io/active-directory/
[glances]:      https://gaviolajosh.github.io/glances/
[chirpy]:       https://github.com/cotes2020/jekyll-theme-chirpy
[nginx]:        https://nginxproxymanager.com/
[docker]:       https://www.docker.com/
[proxmox]:      https://www.proxmox.com/en/proxmox-virtual-environment/overview
