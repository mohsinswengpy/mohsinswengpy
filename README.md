<div align="center">

<img src="assets/banner.svg" alt="Mohsin Khan - Aspiring Network Engineer" width="100%" />

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3000&pause=900&color=049FD9&center=true&vCenter=true&width=700&height=50&lines=Building+Networks+from+the+Ground+Up;Designing+Secure+and+Redundant+Networks;CCNA+Path+%E2%86%92+Network+Automation+%E2%86%92+Cloud;Open+to+Freelance+Network+Projects" alt="Typing SVG" /></a>

<br>

<img src="https://img.shields.io/badge/Cisco-Packet%20Tracer-049FD9?style=for-the-badge&logo=cisco&logoColor=white" />
<img src="https://img.shields.io/badge/Focus-CCNA%20%7C%20Automation%20%7C%20Security-7B2FF7?style=for-the-badge&logo=gnometerminal&logoColor=white" />
<img src="https://img.shields.io/badge/Status-Open%20to%20Work-00C853?style=for-the-badge&logo=upwork&logoColor=white" />

<br><br>

<a href="https://www.linkedin.com/in/mohsin-khan-2002ba3a8"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:mohsin161955@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://mastodon.social/@Mohsin"><img src="https://img.shields.io/badge/Mastodon-2B90D9?style=for-the-badge&logo=mastodon&logoColor=white" /></a>
<a href="https://www.facebook.com/share/p/1BsUQF93ku/"><img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" /></a>

</div>

---

## 👨‍💻 About Me

I'm a **Software Engineering student** building a career in **network engineering**. I design networks that are **reliable, secure and scalable**, and I learn by building: every concept becomes a hands-on lab with documented configs and verification.

| | |
|---|---|
| 🎯 **Goal** | CCNA → CCNP, then Network Automation and Cloud Networking |
| 🔭 **Currently** | Enterprise labs in Cisco Packet Tracer, moving to GNS3 + Python (Netmiko) |
| 🌱 **Next** | BGP, DMVPN, Network Automation, Monitoring (Zabbix / Grafana) |
| 💼 **Open to** | Junior network roles, internships and freelance lab / config work |

---

## 🌐 Featured Project

### 🏢 Enterprise Multi-Branch Network: Lahore HQ ↔ Islamabad Branch

```mermaid
graph LR
    subgraph Lahore_HQ["Lahore Head Office"]
        PC["VLAN 10 / 20 / 30"] --- SW["Core Switches<br/>LACP EtherChannel"]
        SW --- R1["R1-HQ<br/>HSRP Active"]
        SW --- R2["R2-HQ<br/>HSRP Standby"]
    end
    R1 ---|"200.1.1.0/30"| ISP(("R-ISP"))
    ISP ---|"200.2.2.0/30"| RB["R-Islamabad"]
    RB --- LAN["192.168.40.0/24"]
    R1 -. "Site-to-Site IPsec VPN" .- RB
```

**Highlights:** VLAN segmentation · Router-on-a-Stick · HSRP high availability · OSPF · LACP EtherChannel · DHCP · NAT/PAT with VPN exemption · Extended ACLs · Port Security · SSH · Site-to-Site IPsec VPN

---

## 📂 Projects

<table>
<tr>
<td width="50%">
<a href="https://github.com/mohsinswengpy/-Enterprise-Multi-Branch-Infrastructure-Redundant-Network-Architecture">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=mohsinswengpy&repo=-Enterprise-Multi-Branch-Infrastructure-Redundant-Network-Architecture&theme=radical&hide_border=true" />
</a>
</td>
<td width="50%">
<a href="https://github.com/mohsinswengpy/OSPF-Multi-Area-Routing-Cisco-Packet-Tracer">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=mohsinswengpy&repo=OSPF-Multi-Area-Routing-Cisco-Packet-Tracer&theme=radical&hide_border=true" />
</a>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/mohsinswengpy/OSPF-Dynamic-Routing-Failover">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=mohsinswengpy&repo=OSPF-Dynamic-Routing-Failover&theme=radical&hide_border=true" />
</a>
</td>
<td width="50%">
<a href="https://github.com/mohsinswengpy/vlan-segmentation-trunking-lab">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=mohsinswengpy&repo=vlan-segmentation-trunking-lab&theme=radical&hide_border=true" />
</a>
</td>
</tr>
<tr>
<td width="50%">
<a href="https://github.com/mohsinswengpy/dhcp-nat-acl-networking-lab">
<img src="https://github-readme-stats.vercel.app/api/pin/?username=mohsinswengpy&repo=dhcp-nat-acl-networking-lab&theme=radical&hide_border=true" />
</a>
</td>
<td width="50%">

| Skill area | Covered in |
|---|---|
| Switching | VLAN, Trunking, EtherChannel |
| Routing | OSPF Multi-Area, Failover |
| Redundancy | HSRP, Dual paths |
| Services | DHCP, NAT/PAT, ACL |
| Security | Port Security, SSH, IPsec |

</td>
</tr>
</table>

---

## 🛠️ Tech Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=py,cs,cpp,js,html,css,mysql,aws,azure,github,git,linux,vscode&perline=13" />

<br><br>

![Cisco](https://img.shields.io/badge/Cisco_IOS-049FD9?style=for-the-badge&logo=cisco&logoColor=white)
![Packet Tracer](https://img.shields.io/badge/Packet_Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![OSPF](https://img.shields.io/badge/OSPF-0A66C2?style=for-the-badge)
![VLAN](https://img.shields.io/badge/VLAN-7B2FF7?style=for-the-badge)
![HSRP](https://img.shields.io/badge/HSRP-E91E63?style=for-the-badge)
![IPsec VPN](https://img.shields.io/badge/IPsec_VPN-00C853?style=for-the-badge)
![NAT](https://img.shields.io/badge/NAT%2FPAT-FF9800?style=for-the-badge)
![ACL](https://img.shields.io/badge/ACL-F44336?style=for-the-badge)

</div>

---

## 🚀 Roadmap

| Status | Goal |
|:---:|---|
| ✅ | CCNA-level labs: VLAN, OSPF, HSRP, NAT, ACL, IPsec VPN |
| 🔄 | Python network automation with Netmiko (ConfigGuardian) |
| 🔄 | CCNA certification |
| ⏳ | BGP + multi-site WAN (BGP-Bridge) |
| ⏳ | Monitoring with Zabbix / Grafana (NetPulse) |
| ⏳ | Firewall and security lab (FortressNet) |
| ⏳ | CCNP and Cloud Networking (AWS / Azure) |

---

## 📊 GitHub Stats

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=mohsinswengpy&show_icons=true&theme=radical&hide_border=true&count_private=true" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mohsinswengpy&layout=compact&theme=radical&hide_border=true" />

<img src="https://streak-stats.demolab.com/?user=mohsinswengpy&theme=radical&hide_border=true" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=mohsinswengpy&bg_color=0d1117&color=049FD9&line=7B2FF7&point=ffffff&area=true&area_color=7B2FF7&hide_border=true" width="100%" />

<img src="https://github-profile-trophy.vercel.app/?username=mohsinswengpy&theme=radical&no-frame=true&no-bg=true&margin-w=4&row=1&column=7" />

</div>

---

## 🐍 Contribution Snake

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:7B2FF7,100:049FD9&height=3&section=header" width="60%" />

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake.svg" />
  <img alt="Neon contribution snake" src="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake-dark.svg" />
</picture>

<sub>🐍 This snake eats my commits. Every colored square is a lab I built.</sub>

</div>

---

<div align="center">

### 🤝 Need a network designed, configured or troubleshot? Let's connect!

<a href="mailto:mohsin161955@gmail.com"><img src="https://img.shields.io/badge/Message_Me-049FD9?style=for-the-badge&logo=gmail&logoColor=white" /></a>

<img src="https://komarev.com/ghpvc/?username=mohsinswengpy&label=Profile+Views&color=049FD9&style=flat-square" />

<img src="assets/footer.svg" alt="footer" width="100%" />

</div>
