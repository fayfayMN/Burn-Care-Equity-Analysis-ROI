# Burn Care Equity & Economic Impact Analysis
---

## 🔬 Domain Expertise: Burn Care Systems Engineering

This repository integrates structural data from the **National Injury Resource Database (NIRD)** with public health equity frameworks to address the three core challenges defined by the **HeatMap Hackathon**.

---
### 🥇 1st Place Winner: 2026 HeatMap Hackathon (Team 13)
> "Team 13’s submission showcased impactful analysis identifying geographic disparities in burn care access, leveraging integrated data to highlight underserved regions and inform more equitable resource allocation." — **BData Inc, Official Result Announcement**
**Official Team Repository:** [efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis](https://github.com/efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis)

This repository contains the independent technical architecture and economic impact models I developed for the **1st Place** winning solution at the 2026 HeatMap Hackathon, hosted by BData and the American Burn Association. 

While the broader team focused on the Composite Vulnerability Index (CVI), **this work provides the specific ROI engine** that quantifies the financial and clinical burden of geographic burn care disparities in the United States.

---

## 🚀 Core Analysis Pillars

### 1. Referral Network Optimization
**The Problem:** Burn care is highly specialized. Delays in transferring patients from general trauma centers to ABA-verified burn centers significantly increase mortality rates and healthcare costs.
* **Our Analysis:** We modeled the **"Referral Gap"** by identifying Level 1–3 Trauma Centers that lack specialized burn capabilities, pinpointing exactly where the bottlenecks for acute injuries occur in the national pipeline.

### 2. Telemedicine Feasibility & ROI
**The Problem:** Maintaining a full-scale burn center is not financially or operationally feasible for every region, yet specialized expertise is a universal requirement for patient survival.
* **Our Analysis:** We identified **351 specific trauma centers** positioned to serve as "Tele-Burn Hubs." By prioritizing these hubs in identified "burn deserts," we maximize the **Return on Investment (ROI)** for healthcare systems while drastically reducing the economic burden of air-transfers.

### 3. Equitable Access to Care
**The Problem:** Socioeconomic factors and geographic isolation create "hidden" disparities in burn survival rates that state-level data often masks.
* **Our Analysis:** We pivoted from state-level metrics to a high-resolution analysis of **3,135 U.S. counties** using **population-weighted centroids**. This ensures equity priorities are based on actual human density rather than geographic landmass.
---
## 📚 Research Bibliography & Resources

* **The NIRD Framework:** Based on *Development of the National Injury Resource Database* (Lovick et al., 2023).
* **Economic Burden:** Grounded in *The Burden of Burns: An Analysis of Public Health Measures* (Ivanko et al., 2024).
* **Regional Success Models:** Referencing the **Maine regionalized system** for rural mortality benchmarks.
---
## 🚀 Key Technical Contributions

### 1. The $1.12B Healthcare Burden Model
I developed a state-level financial impact model based on the *Huang et al. (2021)* under-referral benchmarks. 

* **Insight:** Identified that California alone faces a **$1.12 Billion** annual burden due to delayed specialized care.
* **Logic:** Modeled the 7% excess infection rate and 66% under-referral rate against state-specific trauma volumes to establish a "conservative floor" for avoidable costs.

### 2. Telemedicine ROI & Spoke Mapping
I engineered the logic to identify "Tele-Burn Hub" candidates by mapping high-volume Tier 1 Trauma Centers to existing Burn Center "Anchors."

* **Efficiency Gain:** My model identified a **$305 Million recovery potential** in California through the activation of 49 specific trauma sites as telemedicine spokes.
* **Granular Analysis:** Performed a comparative study of Illinois vs. California, proving that infrastructure density (number of spokes) must be weighted against population centroids to calculate true ROI.

### 3. Geospatial Equity Engineering
* **Distance Burden:** Calculated the "100-Mile Burden" using population-weighted county centroids and Haversine distance.
* **Vulnerability Correlation:** Integrated CDC Social Vulnerability Index (SVI) data to prove that poverty increases the distance to ABA-verified care by a factor of **1.4x**.

---

## 🌐 Interactive Visualizations

> [!TIP]
> **Explore the Live Dashboard:** [Interactive Burn Care HeatMap](https://fayfaymn.github.io/Burn-Care-Equity-Analysis-ROI/)

I engineered the underlying data pipelines and financial logic (documented in `Burn_Care_ROI_Engine.ipynb`) that power the following layers in this dashboard:

* **Tele-Burn Hub Network:** Identified 498 optimal trauma sites based on population density and referral radius.
* **The Referral Gap:** Modeled the 66% under-referral rate that contributes to the $112M annual avoidable cost floor.
* **Geospatial Burdens:** Calculated the 100-mile "Failure Zones" using population-weighted county centroids.

---

## 🛠️ Tech Stack

| Category | Tools & Resources |
| :--- | :--- |
| **Language** | Python |
| **Libraries** | Pandas, NumPy, Plotly, Folium (Geospatial Visualization) |
| **Data Sources** | NIRD 2023, US Census 2020, CDC/ATSDR SVI 2022, USDA RUCC 2023 |

---

## 📂 Repository Structure
* `Main_ROI_Analysis.ipynb`: The core engine for financial modeling and state-level data integration.
* `Geography_of_Survival_Deck.pptx`: My technical proposal and visual storytelling of the data.
* `Visualizations`: Interactive maps showing the "Burn Deserts" and the proposed Tele-Burn Hub network.

---

## 🏆 Hackathon Recognition
Our team (Team 13) was awarded **First Place** for our impactful analysis of geographic disparities. This repository showcases the specific data infrastructure I built to support that winning vision.
> "19 teams. 90+ participants. One shared belief that better data leads to better care. Here's what our winners discovered:

🥇 First Place: Team 13 Josh Spitzer-Resnick, Emmanuel Fle Chea, MPH, Shreya Pramanik, Feifei Li and Lance Killian McDonald.

Team 13’s submission showcased impactful analysis identifying geographic disparities in burn care access, leveraging integrated data to highlight underserved regions and inform more equitable resource allocation. " — **BData Inc, Official Result Announcement**
