<div align="center">

<img src="banner.svg" alt="Mohsin Khan, aspiring DevOps engineer. A packet travels from a lab network through an IPsec tunnel to an AWS VPC." width="100%" />

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=3200&pause=1000&color=5EEAD4&center=true&vCenter=true&width=760&height=45&lines=Networks+first.+Then+Linux.+Then+Cloud.;CCNA+%E2%86%92+Linux+%E2%86%92+AWS+%E2%86%92+Automation;Designing+secure+and+redundant+networks;Open+to+freelance+network+projects" alt="Typing SVG" /></a>

<br/>

<a href="https://www.linkedin.com/in/mohsin-khan-2002ba3a8"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
<a href="mailto:mohsin161955@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
<a href="https://mastodon.social/@Mohsin"><img src="https://img.shields.io/badge/Mastodon-2B90D9?style=for-the-badge&logo=mastodon&logoColor=white" alt="Mastodon" /></a>
<a href="https://www.facebook.com/share/p/1BsUQF93ku/"><img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Facebook" /></a>

</div>

<img src="divider.svg" alt="" width="100%" />

<img src="sec-about.svg" alt="whoami" width="100%" />

I am a Software Engineering student who builds enterprise networks in the lab: VLANs, OSPF, HSRP, NAT, ACLs and IPsec VPNs. I am now moving toward **DevOps** by learning three things side by side: **CCNA**, **Linux** and **AWS**. After that comes Git, Docker, Terraform, CI/CD and Kubernetes.

I also build real software. I wrote a desktop POS system that a working pharmacy uses.

<div align="center">

<img src="https://img.shields.io/badge/Networking_labs-5-049FD9?style=for-the-badge&labelColor=0d1117&logo=cisco&logoColor=white" alt="Networking labs: 5" />
<img src="https://img.shields.io/badge/Power_BI_dashboards-2-F2C811?style=for-the-badge&labelColor=0d1117&logo=powerbi&logoColor=white" alt="Power BI dashboards: 2" />
<img src="https://img.shields.io/badge/ML_and_data_projects-5-FF2D87?style=for-the-badge&labelColor=0d1117&logo=scikitlearn&logoColor=white" alt="ML and data projects: 5" />
<img src="https://img.shields.io/badge/Commercial_POS-1-22E58A?style=for-the-badge&labelColor=0d1117&logo=python&logoColor=white" alt="Commercial POS: 1" />

</div>

<img src="divider.svg" alt="" width="100%" />

<img src="sec-journey.svg" alt="quest status" width="100%" />

<div align="center">
<img src="quest.svg" alt="DevOps quest log: networking labs cleared, CCNA, Linux and AWS in progress, then Git and Docker, IaC and CI/CD, and Kubernetes ahead." width="100%" />
</div>

<img src="divider.svg" alt="" width="100%" />

<img src="sec-terminal.svg" alt="tail -f lab-session.log" width="100%" />

<div align="center">
<img src="terminal.svg" alt="Animated terminal: an IPsec status check, an SSH uptime check and the next tools to learn. Illustrative." width="860" />
</div>

<img src="divider.svg" alt="" width="100%" />

<img src="sec-featured.svg" alt="cat featured-project.md" width="100%" />

### Enterprise Multi-Branch Network: Lahore HQ and Islamabad Branch

<img src="featured-map.svg" alt="Enterprise Multi-Branch Network map" width="100%" />

**Highlights:** VLAN segmentation, Router-on-a-Stick, HSRP high availability, OSPF, LACP EtherChannel, DHCP, NAT/PAT with VPN exemption, extended ACLs, port security, SSH, site-to-site IPsec VPN.

<img src="divider.svg" alt="" width="100%" />

<img src="sec-projects.svg" alt="ls networking-projects/" width="100%" />

<table>
<tr>
<td width="50%"><a href="https://github.com/mohsinswengpy/-Enterprise-Multi-Branch-Infrastructure-Redundant-Network-Architecture"><img src="p1-enterprise.svg" alt="Enterprise Multi-Branch Network" width="100%" /></a></td>
<td width="50%"><a href="https://github.com/mohsinswengpy/OSPF-Multi-Area-Routing-Cisco-Packet-Tracer"><img src="p2-ospf-multiarea.svg" alt="OSPF Multi-Area Routing" width="100%" /></a></td>
</tr>
<tr>
<td width="50%"><a href="https://github.com/mohsinswengpy/OSPF-Dynamic-Routing-Failover"><img src="p3-ospf-failover.svg" alt="OSPF Dynamic Routing Failover" width="100%" /></a></td>
<td width="50%"><a href="https://github.com/mohsinswengpy/vlan-segmentation-trunking-lab"><img src="p4-vlan.svg" alt="VLAN Segmentation and Trunking" width="100%" /></a></td>
</tr>
<tr>
<td width="50%"><a href="https://github.com/mohsinswengpy/dhcp-nat-acl-networking-lab"><img src="p5-services.svg" alt="DHCP, NAT and ACL Networking Lab" width="100%" /></a></td>
<td width="50%"><img src="p6-configguardian.svg" alt="ConfigGuardian: network automation, coming soon" width="100%" /></td>
</tr>
</table>

<details>
<summary><b>Enterprise Multi-Branch Network (Lahore HQ and Islamabad)</b></summary>

**The problem:** A company with two offices needs them to talk to each other securely over the internet, and the head office must keep working even if one gateway router fails.

**What I built:** A Head Office in Lahore (HR, IT and Server VLANs, access and core switches, two routers) connected through an ISP to a Branch Office in Islamabad.

**How it works:**
- **VLANs 10 / 20 / 30** separate HR, IT and Servers, with **Router-on-a-Stick** providing inter-VLAN routing.
- **HSRP** gives the PCs one virtual gateway. R1-HQ is Active (priority 110, preempt on) and R2-HQ is Standby (priority 100), so R2-HQ takes over if R1-HQ fails.
- **LACP EtherChannel** bundles the core switch links for more bandwidth and link redundancy.
- **OSPF Area 0** exchanges routes between the two HQ routers.
- **DHCP** assigns addresses, **NAT/PAT** gives internet access, and **NAT exemption** keeps VPN traffic out of NAT so the tunnel matches correctly.
- **Extended ACLs, port security and SSH** protect the network and management access.
- **Site-to-Site IPsec VPN** encrypts traffic between Lahore and Islamabad across the ISP.

**How I checked it:** `show standby brief`, `show ip ospf neighbor`, `show etherchannel summary`, `show crypto isakmp sa`, `show ip nat translations`, and pings between the two sites.

**Known limitation:** Gateway redundancy covers Lahore only. Islamabad has one router, and VPN failover for R2-HQ is a planned improvement.

</details>

<details>
<summary><b>OSPF Multi-Area Routing</b></summary>

**The problem:** In a big network, a single OSPF area makes every router hold every detail of the whole topology, which does not scale.

**What I built:** A lab with **Area 0 (backbone)** and **Area 1** across three routers, connecting two end-user networks.

**How it works:** An **Area Border Router (ABR)** sits between the two areas and passes summarised routes between them. Routes from the other area show up as inter-area (`O IA`) routes, so routing tables stay smaller and changes affect fewer routers.

**How I checked it:** `show ip ospf neighbor`, `show ip route`, and a ping between the two end-user networks.

</details>

<details>
<summary><b>OSPF Dynamic Routing with Failover</b></summary>

**The problem:** If the only path to the ISP breaks, users lose internet. Networks need a backup path that takes over without manual work.

**What I built:** A network with **two paths to an ISP** and a server reachable across it, using OSPF.

**How it works:** OSPF learns both paths and prefers the best one. When I bring the primary link down, OSPF removes that route, recalculates and moves traffic to the backup path automatically. The server stays reachable.

**How I checked it:** Routing table before and after the failure, and ping tests while the link was down.

</details>

<details>
<summary><b>VLAN Segmentation and Trunking</b></summary>

**The problem:** Putting every department on one flat network is slow and insecure, because every device hears every broadcast.

**What I built:** A switched lab where departments are split into **VLANs** on shared switches, with access ports, **802.1Q trunks**, per-VLAN addressing and connectivity tests inside and between VLANs. I also practised troubleshooting typical problems such as a wrong VLAN on a port.

</details>

<details>
<summary><b>DHCP, NAT and ACL Networking Lab</b></summary>

**The problem:** A network needs addresses handed out automatically, a way for private devices to reach the internet, and rules about what traffic is allowed.

**What I built:** A lab that configures **DHCP** for automatic addressing, **NAT/PAT** so many private devices share one public address, and **ACLs** to allow or block specific traffic.

</details>

<details>
<summary><b>ConfigGuardian: network automation (in progress)</b></summary>

**The problem:** Backing up and checking router configurations by hand is slow and error-prone.

**Plan:** A **Python + Netmiko** tool, tested in GNS3, that connects to routers over SSH, saves their configurations, and checks settings such as SSH and logging. It will also read OSPF neighbor state and produce a simple report. The code will be published when it is finished.

</details>

### On the bench next

| Status | Build |
|:---:|---|
| 🔄 | **Hybrid cloud lab:** a lab network connected to an AWS VPC over a Site-to-Site IPsec VPN |
| 🔄 | **ConfigGuardian:** Python and Netmiko config backup and audit |
| ⏳ | **BGP and multi-site WAN**, then **monitoring** with Zabbix and Grafana |

<img src="divider.svg" alt="" width="100%" />

<img src="sec-software.svg" alt="cat desktop-software.md" width="100%" />

### Sheraz Pharmacy POS: desktop software for a real pharmacy

<img src="pos-card.svg" alt="Sheraz Pharmacy POS interface preview (illustration)" width="100%" />

<div align="center">

*A complete point-of-sale and inventory system that runs as a normal Windows program. No internet, no monthly fees.*

</div>

| | What it does |
|---|---|
| 🛒 | **Fast billing:** search a medicine, add it to the cart and print a PDF bill in seconds |
| 🏷 | **Flexible pricing:** a default discount per medicine, and a custom price with a live price-variance indicator |
| 📦 | **Inventory control:** stock, cost, price, expiry date and low-stock alerts |
| 🔄 | **Sales returns:** return items against an invoice and the stock goes back automatically |
| 📊 | **Live dashboard:** today's sales, gross profit and stock level at a glance |
| 📑 | **Excel import and export:** move the medicine list in and out |
| 💾 | **One-click backup** of the whole database |
| 🌙 | **Modern dark interface** that is easy on the eyes during long shifts |

**Built with:** `Python` · `PyQt6` · `SQLite` · `ReportLab` · `OpenPyXL`

> 🔒 This is closed-source commercial software. The source code is not public.

<img src="divider.svg" alt="" width="100%" />

<img src="sec-data.svg" alt="ls data-and-ml/" width="100%" />

<details>
<summary><b>Data analytics and machine learning projects (7)</b></summary>

<br/>

| Project | What it does | Tools |
|---|---|---|
| [**superstore-sales-analysis-powerbi**](https://github.com/mohsinswengpy/superstore-sales-analysis-powerbi) | Interactive dashboard analysing Superstore sales, profit, product, customer / region and shipping data across 4 report pages. | Power BI |
| [**ecommerce-sales-dashboard**](https://github.com/mohsinswengpy/ecommerce-sales-dashboard) | E-commerce sales dashboard showing yearly revenue, profit trends and regional performance. | Power BI |
| [**Loan-Status-Prediction-SVM**](https://github.com/mohsinswengpy/Loan-Status-Prediction-SVM) | Predicts loan approval status to reduce manual bias and support faster, data-driven lending decisions. | Python, SVM, Jupyter |
| [**House-Price-Prediction-**](https://github.com/mohsinswengpy/House-Price-Prediction-) | Predicts house prices with an XGBoost Regressor: preprocessing, EDA, training and evaluation. | Python, Pandas, Scikit-learn, XGBoost |
| [**car-price-prediction**](https://github.com/mohsinswengpy/car-price-prediction) | Predicts the selling price of used cars with regression on year, fuel type and transmission. | Python, Jupyter |
| [**-Fake-News-Prediction**](https://github.com/mohsinswengpy/-Fake-News-Prediction) | Classifies news articles as Real or Fake from title, author and text. | Python, NLTK, Scikit-learn |
| [**rock-and-mine**](https://github.com/mohsinswengpy/rock-and-mine) | End-to-end data science project using predictive analytics to help optimise agricultural productivity. | Python |

</details>

<img src="divider.svg" alt="" width="100%" />

<img src="sec-stack.svg" alt="cat stack.txt" width="100%" />

<div align="center">

<img src="https://img.shields.io/badge/Cisco-IOS-049FD9?style=flat-square&logo=cisco&logoColor=white" alt="Cisco IOS" />
<img src="https://img.shields.io/badge/Packet_Tracer-lab-1BA0D7?style=flat-square" alt="Packet Tracer" />
<img src="https://img.shields.io/badge/GNS3-lab-6C3FD1?style=flat-square" alt="GNS3" />
<img src="https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54" alt="Python" />
<img src="https://img.shields.io/badge/Linux-learning-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux, learning" />
<img src="https://img.shields.io/badge/AWS-learning-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white" alt="AWS, learning" />
<img src="https://img.shields.io/badge/CCNA-in_progress-F59E0B?style=flat-square&logo=cisco&logoColor=white" alt="CCNA, in progress" />
<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
<img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black" alt="Power BI" />

</div>

<img src="divider.svg" alt="" width="100%" />

<img src="sec-stats.svg" alt="git log --stat" width="100%" />

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=mohsinswengpy&show_icons=true&hide_border=false&bg_color=0d1117&title_color=5eead4&text_color=c9d1d9&icon_color=fbbf24&border_color=1b2c4a&count_private=true" alt="GitHub stats" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mohsinswengpy&layout=compact&bg_color=0d1117&title_color=5eead4&text_color=c9d1d9&border_color=1b2c4a" alt="Top languages" />

<img src="https://streak-stats.demolab.com/?user=mohsinswengpy&background=0D1117&border=1B2C4A&stroke=1B2C4A&ring=5EEAD4&fire=FBBF24&currStreakNum=FFFFFF&sideNums=FFFFFF&currStreakLabel=5EEAD4&sideLabels=8FB3C9&dates=5D7E95" alt="Contribution streak" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=mohsinswengpy&bg_color=0d1117&color=5eead4&line=22d3ee&point=ffffff&area=true&area_color=22d3ee&hide_border=true" width="100%" alt="Contribution graph" />

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake.svg" />
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake-dark.svg" />
</picture>

</div>

<img src="divider.svg" alt="" width="100%" />

<img src="sec-contact.svg" alt="mail -s hello mohsin" width="100%" />

<div align="center">

### Need a network designed, configured or troubleshot? Or custom business software?

<a href="mailto:mohsin161955@gmail.com"><img src="https://img.shields.io/badge/Message_me-5EEAD4?style=for-the-badge&logo=gmail&logoColor=0d1117" alt="Message me" /></a>

<img src="https://komarev.com/ghpvc/?username=mohsinswengpy&label=Profile+Views&color=22d3ee&style=flat-square" alt="Profile views" />

</div>
