<div align="center">

<img src="banner.svg" alt="Mohsin Khan - Software Engineering Student | Aspiring Network Engineer" width="100%" />

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=20&duration=3200&pause=1000&color=8FDCFF&center=true&vCenter=true&width=720&height=45&lines=Building+Networks+from+the+Ground+Up;Designing+Secure+and+Redundant+Networks;CCNA+Path+%E2%86%92+Network+Automation+%E2%86%92+Cloud;Open+to+Freelance+Network+Projects" alt="Typing SVG" /></a>

<br>

<a href="https://www.linkedin.com/in/mohsin-khan-2002ba3a8"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
<a href="mailto:mohsin161955@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
<a href="https://mastodon.social/@Mohsin"><img src="https://img.shields.io/badge/Mastodon-2B90D9?style=for-the-badge&logo=mastodon&logoColor=white" /></a>
<a href="https://www.facebook.com/share/p/1BsUQF93ku/"><img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" /></a>

</div>

<br>

<img src="h-about.svg" alt="About Me" width="100%" />

<img src="about.svg" alt="About Mohsin Khan: Software Engineering student building a career in network engineering" width="100%" />

<br>

FEATURED PROJECT

<img src="h-featured.svg" alt="Featured Project" width="100%" />

### 🏢 Enterprise Multi-Branch Network: Lahore HQ ↔ Islamabad Branch

<img src="featured-map.svg" alt="Enterprise Multi-Branch Network map" width="100%" />

**Highlights:** VLAN segmentation · Router-on-a-Stick · HSRP high availability · OSPF · LACP EtherChannel · DHCP · NAT/PAT with VPN exemption · Extended ACLs · Port Security · SSH · Site-to-Site IPsec VPN

<br>

<img src="h-projects.svg" alt="Projects" width="100%" />

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

### 📖 Project Details

<sub>Click a project to read the full explanation.</sub>

<details>
<summary><b>🏢 Enterprise Multi-Branch Network (Lahore HQ ↔ Islamabad)</b></summary>

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

**Skills:** High availability, WAN design, IPsec VPN, enterprise planning.

</details>

<details>
<summary><b>🌐 OSPF Multi-Area Routing</b></summary>

**The problem:** In a big network, a single OSPF area makes every router hold every detail of the whole topology, which does not scale.

**What I built:** A lab with **Area 0 (backbone)** and **Area 1** across three routers, connecting two end-user networks.

**How it works:**
- An **Area Border Router (ABR)** sits between the two areas and passes summarised routes between them.
- Routes learned from the other area show up as **inter-area (`O IA`)** routes.
- Because details stay inside each area, the routing tables stay smaller and changes affect fewer routers.

**How I checked it:** `show ip ospf neighbor`, `show ip route`, and a ping between the two end-user networks.

**Skills:** Multi-area OSPF, ABR role, reading routing tables.

</details>

<details>
<summary><b>🔁 OSPF Dynamic Routing with Failover</b></summary>

**The problem:** If the only path to the ISP breaks, users lose internet. Networks need a backup path that takes over without manual work.

**What I built:** A network with **two paths to an ISP** and a server reachable across it, using OSPF as the routing protocol.

**How it works:**
- OSPF learns both paths and prefers the best one.
- When I bring the primary link down, OSPF removes that route, recalculates and switches traffic to the backup path automatically.
- The server stays reachable during and after the change.

**How I checked it:** Routing table before and after the failure, and ping tests while the link was down.

**Skills:** Dynamic routing, redundancy, convergence.

</details>

<details>
<summary><b>🧩 VLAN Segmentation & Trunking</b></summary>

**The problem:** Putting every department on one flat network is slow and insecure, because every device hears every broadcast.

**What I built:** A switched lab where departments are split into **VLANs** on shared switches.

**How it works:**
- VLANs are created and ports are assigned as **access ports** to the right VLAN.
- Links between switches are **802.1Q trunks**, which carry traffic for many VLANs over one cable using tags.
- IP addressing is set up per VLAN, and connectivity is tested inside each VLAN and between them.
- I also practised troubleshooting typical problems such as a wrong VLAN on a port.

**Skills:** Layer 2 switching, VLANs, trunking, troubleshooting.

</details>

<details>
<summary><b>🛡️ DHCP, NAT & ACL Networking Lab</b></summary>

**The problem:** A network needs addresses handed out automatically, a way for private devices to reach the internet, and rules about what traffic is allowed.

**What I built:** A lab that configures three core network services.

**How it works:**
- **DHCP** gives devices their IP settings automatically, so nobody has to type them in.
- **NAT/PAT** translates private addresses to a public one so many devices can share a single internet address.
- **ACLs** allow or block specific traffic, which is the first layer of network security.

**Skills:** Network services, traffic filtering, basic security.

</details>

<details>
<summary><b>⚙️ ConfigGuardian: Network Automation (in progress)</b></summary>

**The problem:** Backing up and checking router configurations by hand is slow and error-prone.

**Plan:** A **Python + Netmiko** tool, tested in GNS3, that connects to routers over SSH, saves their configurations, and checks settings such as SSH and logging. It will also read OSPF neighbor state and produce a simple report.

**Status:** In development. The code will be published when it is finished.

</details>

<br>

<img src="h-data.svg" alt="Data and ML Projects" width="100%" />

<div align="center">

*Beyond networking: data analysis and machine learning projects built with Python and Power BI.*

</div>

### 📊 Data Analytics (Power BI)

| Project | What it does | Tools |
|---|---|---|
| [**superstore-sales-analysis-powerbi**](https://github.com/mohsinswengpy/superstore-sales-analysis-powerbi) | Interactive dashboard analysing Superstore sales, profit, product, customer / region and shipping data across 4 report pages. | ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black) |
| [**ecommerce-sales-dashboard**](https://github.com/mohsinswengpy/ecommerce-sales-dashboard) | E-commerce sales dashboard showing yearly revenue, profit trends and regional performance. | ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black) |

### 🤖 Machine Learning

| Project | What it does | Tools |
|---|---|---|
| [**Loan-Status-Prediction-SVM**](https://github.com/mohsinswengpy/Loan-Status-Prediction-SVM) | Predicts loan approval status to reduce manual bias, speed up processing and support faster, data-driven lending decisions. | ![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![SVM](https://img.shields.io/badge/SVM-7B2FF7?style=flat-square) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) |
| [**House-Price-Prediction-**](https://github.com/mohsinswengpy/House-Price-Prediction-) | Predicts house prices with an XGBoost Regressor, covering data preprocessing, EDA, model training and evaluation. | ![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![XGBoost](https://img.shields.io/badge/XGBoost-049FD9?style=flat-square) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) |
| [**car-price-prediction**](https://github.com/mohsinswengpy/car-price-prediction) | Predicts the selling price of used cars using regression analysis on features like year, fuel type and transmission. | ![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![Regression](https://img.shields.io/badge/Regression-FF2D87?style=flat-square) ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white) |
| [**-Fake-News-Prediction**](https://github.com/mohsinswengpy/-Fake-News-Prediction) | Classifies news articles as Real or Fake based on their title, author and text content. | ![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![NLTK](https://img.shields.io/badge/NLTK-22E58A?style=flat-square) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) |
| [**rock-and-mine**](https://github.com/mohsinswengpy/rock-and-mine) | End-to-end data science project that uses predictive analytics to help optimise agricultural productivity. | ![Python](https://img.shields.io/badge/Python-3670A0?style=flat-square&logo=python&logoColor=ffdd54) ![Predictive Analytics](https://img.shields.io/badge/Predictive_Analytics-7B2FF7?style=flat-square) |

### 📖 Project Details

<sub>Click a project to read the full explanation.</sub>

<details>
<summary><b>📊 Superstore Sales Analysis (Power BI)</b></summary>

**The problem:** A retail business has thousands of sales rows but no quick way to see what is selling, what is profitable, and where.

**What I built:** An **interactive Power BI dashboard** spread over **4 report pages**.

**What it shows:**
- Sales and profit performance
- Product-level analysis
- Customer and regional breakdown
- Shipping data

**Why it is useful:** A manager can filter the visuals and spot strong and weak products or regions without reading raw tables.

**Skills:** Data modelling, DAX / visuals, dashboard design, business insight.

</details>

<details>
<summary><b>🛒 E-commerce Sales Dashboard (Power BI)</b></summary>

**The problem:** An online store needs a simple view of how the business is doing over time and by region.

**What I built:** A Power BI dashboard that analyses **yearly revenue, profit trends and regional performance**.

**Why it is useful:** It turns sales records into charts that show growth, slow periods and the best-performing regions.

**Skills:** Data visualisation, KPI design, trend analysis.

</details>

<details>
<summary><b>🏦 Loan Status Prediction (SVM)</b></summary>

**The problem:** Deciding loan approvals by hand is slow and can be biased.

**What I built:** A machine-learning model using a **Support Vector Machine (SVM)** that predicts whether a loan will be approved.

**Approach:** Prepare and clean the applicant data, train the SVM classifier, and evaluate how well it predicts loan status.

**Why it is useful:** It supports faster, data-driven lending decisions and reduces manual bias.

**Skills:** Classification, data preprocessing, model evaluation (Python, Scikit-learn).

</details>

<details>
<summary><b>🏠 House Price Prediction (XGBoost)</b></summary>

**The problem:** Pricing a house depends on many factors, and guessing is unreliable.

**What I built:** A regression project that predicts house prices with an **XGBoost Regressor**.

**Approach:**
1. **Data preprocessing:** cleaning and preparing the data.
2. **EDA:** exploring patterns and relationships in the data.
3. **Model training:** fitting the XGBoost model.
4. **Evaluation:** measuring how close the predictions are to real prices.

**Tools:** Python, Pandas, Scikit-learn, XGBoost.

**Skills:** Regression, feature handling, model evaluation.

</details>

<details>
<summary><b>🚗 Car Price Prediction</b></summary>

**The problem:** Sellers and buyers of used cars need a fair price estimate.

**What I built:** A machine-learning project that predicts the **selling price of used cars** with **regression analysis**.

**Approach:** Use features such as the car's **year, fuel type and transmission** to train a model, then check how accurate its predictions are.

**Skills:** Regression, categorical feature handling, model evaluation (Python).

</details>

<details>
<summary><b>📰 Fake News Prediction</b></summary>

**The problem:** Fake news spreads quickly and is hard to spot by reading alone.

**What I built:** A machine-learning model that classifies a news article as **Real or Fake** using its **title, author and text**.

**Approach:** Clean and process the text with **NLTK**, turn it into features, and train a classifier with **Scikit-learn**.

**Skills:** Natural language processing, text classification (Python, NLTK, Scikit-learn).

</details>

<details>
<summary><b>🌾 Rock and Mine: Predictive Analytics</b></summary>

**The problem:** Raw field data is hard to turn into useful decisions.

**What I built:** An **end-to-end data science project** that uses predictive analytics to help **optimise agricultural productivity**, connecting raw data to practical, data-driven decisions.

**Skills:** End-to-end data science workflow, predictive modelling (Python).

</details>

<br>

<img src="h-stack.svg" alt="Tech Stack" width="100%" />

<img src="tech-stack.svg" alt="Tech Stack: networking, programming, cloud and tools" width="100%" />

<br>

<img src="h-roadmap.svg" alt="Roadmap" width="100%" />

| Status | Goal |
|:---:|---|
| ✅ | CCNA-level labs: VLAN, OSPF, HSRP, NAT, ACL, IPsec VPN |
| 🔄 | Python network automation with Netmiko (ConfigGuardian) |
| 🔄 | CCNA certification |
| ⏳ | BGP + multi-site WAN (BGP-Bridge) |
| ⏳ | Monitoring with Zabbix / Grafana (NetPulse) |
| ⏳ | Firewall and security lab (FortressNet) |
| ⏳ | CCNP and Cloud Networking (AWS / Azure) |

<br>

<img src="h-stats.svg" alt="GitHub Stats" width="100%" />

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=mohsinswengpy&show_icons=true&hide_border=false&bg_color=0d1117&title_color=049FD9&text_color=c9d1d9&icon_color=7B2FF7&border_color=1f2a44&count_private=true" />
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mohsinswengpy&layout=compact&bg_color=0d1117&title_color=049FD9&text_color=c9d1d9&border_color=1f2a44" />

<img src="https://streak-stats.demolab.com/?user=mohsinswengpy&background=0D1117&border=1F2A44&stroke=1F2A44&ring=049FD9&fire=FF2D87&currStreakNum=FFFFFF&sideNums=FFFFFF&currStreakLabel=049FD9&sideLabels=8FB3C9&dates=5D7E95" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=mohsinswengpy&bg_color=0d1117&color=049FD9&line=7B2FF7&point=ffffff&area=true&area_color=7B2FF7&hide_border=true" width="100%" />

</div>

<br>

<img src="h-snake.svg" alt="Contribution Snake" width="100%" />

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake.svg" />
  <img alt="Neon contribution snake" src="https://raw.githubusercontent.com/mohsinswengpy/mohsinswengpy/output/github-snake-dark.svg" />
</picture>

</div>

---

<div align="center">

### 🤝 Need a network designed, configured or troubleshot? Let's connect!

<a href="mailto:mohsin161955@gmail.com"><img src="https://img.shields.io/badge/Message_Me-049FD9?style=for-the-badge&logo=gmail&logoColor=white" /></a>

<img src="https://komarev.com/ghpvc/?username=mohsinswengpy&label=Profile+Views&color=049FD9&style=flat-square" />

<img src="footer.svg" alt="footer" width="100%" />

</div>
