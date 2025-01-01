---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
---

Hello my name is Josh, and here I'll be posting update on the various projects and homelab technologies I'm working with.  
This site is hosted using [GitHub Pages][github-pages] with a fork of a [Jekyll][jekyll] theme as the main HTML coding.  

Current *8/1/24* Server Setup is a:  
* Dell Poweredge R720:  
  - Dual 8 Core Xeon E5-2665 2.4GHz CPUs
    - (plans are to lower overall TDP to dual 10 Core Xeon E5-2648L V2 1.9GHZ or a single 12 Core Xeon E5-2695 V2 2.4GHz)
  - 64Gb DDR3 1600MT/s ECC RAM
    - (also plan to get more because it's so cheap)
  - 2 x 256Gb Sata SSDs running in a mirrored RAID 1 config
  - 4 x 4Tb Sata HDDs running in RAID 1 as well
  - 4 x 1Gb port NIC
  - PERC H710p Mini RAID controller flashed into IT mode

  - Current Services:
    - [PiHole DNS][pihole]
    - [DuckDNS][duckdns]
    - [Portainer][portainer]
    - ~~GNS3~~ (switched to EVE-NG for now)
    - [Wireguard][wireguard]
    - [Glances][glances]
    - [Dashy][dashy]
    - [EVE-NG][eve-ng]
    - [Active Directory][ad] Through a Windows Server 2019 Test VM
* Main computer/[LLama3][llama3] host with a Ryzen 5 5600x, Radeon RX 6600XT, 32GB DDR4 RAM, 1TB NVME SSD  

Current Networking Hardware:  
* Cisco SG300-10 1Gb 10 port manage switch
* TP-Link tl-sg105e 1GB 5 port managed switch
* TP-Link POE injector
* TP-Link EAP223
* APC UPS BE550G
* Rosewill 25U 4 post adjustable rack

# Future Plans
- [ ] Organize my current homelab setup better
- [x] ~~Set up a dashboard ([Dashy?](https://dashy.to/)) for quick access all my services~~ (5/12/24)  
- [ ] Learn more about [Ansible](https://www.ansible.com/) and [Terraform](https://www.terraform.io/) and see if deploying them would be useful  
  - [ ] Learn YAML  
- [ ] [Ollama](https://ollama.com/library/llama3) seems interesting, but I'm unsure if I could reasonably run it 24/7 with my current resources  
- [x] Get a larger (> 8 port) POE+ switch
  - [ ] Potentially move away from decentralized security and utilize a self-hosted NVR
- [ ] Create a NAS machine(s)
- [ ] Locally create SSL certificates for my services
- [ ] Get a standalone PFsense/OpenWRT/OPNsense device

[github-pages]: https://pages.github.com/
[jekyll]:       http://jekyllthemes.org/
[pihole]:       https://gaviolajosh.github.io/pihole-setup/
[wireguard]:    https://gaviolajosh.github.io/wireguard-setup/
[dashy]:        https://gaviolajosh.github.io/dashy-setup/
[llama3]:       https://ollama.com/
[eve-ng]:       https://gaviolajosh.github.io/eve-ng/
[portainer]:    https://www.portainer.io/
[duckdns]:      https://www.duckdns.org/
[ad]:           https://gaviolajosh.github.io/active-directory/
[glances]:      https://gaviolajosh.github.io/glances/

