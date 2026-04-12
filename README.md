# Burn Care Equity & Economic Impact Analysis

This project quantifies the economic and clinical impact of delayed burn care access in the U.S., identifying over $1B in avoidable costs (specifically modeled for **Texas**) and proposing a telemedicine optimization strategy to improve equity and system efficiency.

---

## 🔬 Domain Expertise: Burn Care Systems Engineering

This repository integrates structural data from the **National Injury Resource Database (NIRD)** with public health equity frameworks to address the three core challenges defined by the **HeatMap Hackathon**.

---

### 🥇 1st Place Winner: 2026 HeatMap Hackathon (Team 13)
> "Team 13’s submission showcased impactful analysis identifying geographic disparities in burn care access, leveraging integrated data to highlight underserved regions and inform more equitable resource allocation." — **BData Inc, Official Result Announcement**

**Official Team Repository:** [efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis](https://github.com/efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis)

This repository contains the independent technical architecture and economic impact models I developed for the **1st Place** winning solution.

---

## 🚀 Core Analysis Pillars

### 1. Referral Network Optimization
**The Problem:** Burn care is highly specialized. Delays in transferring patients from general trauma centers to ABA-verified burn centers significantly increase mortality rates and healthcare costs.
* **Our Analysis:** We modeled the **"Referral Gap"** by identifying the **498** Level 1–3 Trauma Centers that lack specialized burn capabilities, pinpointing exactly where the bottlenecks for acute injuries occur in the national pipeline.

### 2. Telemedicine Feasibility & ROI
**The Problem:** Maintaining a full-scale burn center is not financially or operationally feasible for every region, yet specialized expertise is a universal requirement for patient survival.
* **Our Analysis:** We identified **351 specific trauma centers** positioned to serve as "Tele-Burn Hubs." By prioritizing these hubs in identified "burn deserts," we maximize the **Return on Investment (ROI)** for healthcare systems while drastically reducing the economic burden of air-transfers.

### 3. Equitable Access to Care
**The Problem:** Socioeconomic factors and geographic isolation create "hidden" disparities in burn survival rates that state-level data often masks.
* **Our Analysis:** We pivoted from state-level metrics to a high-resolution analysis of **3,221 U.S. counties** using **population-weighted centroids** (Census 2020). This ensures equity priorities are based on actual human density rather than geographic landmass.

---

## 📚 Research Bibliography & Resources

* **The NIRD Framework:** Based on *Development of the National Injury Resource Database* (Lovick et al., 2023).
* **Economic Burden:** Grounded in *The Burden of Burns: An Analysis of Public Health Measures* (Ivanko et al., 2024).
* **Regional Success Models:** Referencing the **Maine regionalized system** for rural mortality benchmarks.

---

## 🚀 Key Technical Contributions

### 1. The Referral Gap & Systemic Inefficiencies

I developed a state-level referral gap analysis based on the NIRD trauma center data.

**Insight:** The national referral gap includes **498 trauma centers** (Level 1–3) that lack specialized burn capabilities. **Texas** has the highest volume of such centers (**38 trauma centers without burn capability**), representing a primary target for telemedicine intervention and referral network optimization.

**Logic:** By mapping the distribution of trauma centers against existing ABA-verified burn centers, we identified where the acute care pipeline is most severely bottlenecked, establishing a data-driven foundation for prioritizing telemedicine hub activation.

### 2. Telemedicine ROI & Spoke Mapping

I engineered the logic to identify "Tele-Burn Hub" candidates by scoring trauma centers based on trauma level, bed size, and proximity to burn care deserts.

* **High-Priority Hubs:** My model identified **351 high-priority telemedicine sites nationally** (score ≥ 5), representing trauma centers best positioned to serve as telemedicine spokes.
* **State-Level Targeting:** **California** has the highest number of telemedicine candidates (**49 sites**), followed by Texas (38) and Illinois (26), making these states primary targets for telemedicine network implementation.
* **Granular Analysis:** By weighting infrastructure density against population centroids, the model prioritizes hubs that maximize geographic coverage and patient access.

**Methodology:** Telemedicine opportunity score = 3 pts (trauma without burn) + 2 pts (Level 1 trauma) + 1.5 pts (Level 2 trauma) + 0.5–1 pt (bed size quartiles).

### 3. Geospatial Equity Engineering

* **Distance Burden:** Calculated the "100-Mile Burden" for **3,221 U.S. counties** using population-weighted centroids and Haversine distance, identifying states where >50% of counties are beyond 100 miles from a burn center (AK, ND, MT, SD, ID, WY, PR).
* **Vulnerability Integration:** Integrated CDC Social Vulnerability Index (SVI) data including poverty (EP_POV150), minority status (EP_MINRTY), disability (EP_DISABL), and vehicle access (EP_NOVEH) into the state-level equity framework.
* **Data Availability:** SVI metrics were merged with access metrics, enabling future correlation analysis between social vulnerability and geographic distance to ABA-verified care.

---

## 🌐 Interactive Visualizations

> [!TIP]
> **Explore the Live Dashboard:** [Interactive Burn Care HeatMap](https://fayfaymn.github.io/Burn-Care-Equity-Analysis-ROI/)

I engineered the underlying data pipelines (documented in `Burn_Care_ROI_Engine.ipynb`) that power the following layers in this dashboard:

* **Tele-Burn Hub Network:** Identified **351** high-priority trauma sites (score ≥ 5) based on trauma level, bed size, and referral gap status.
* **The Referral Gap:** Modeled the **66% under-referral rate** affecting **498 trauma centers** (88% of all L1–L3 trauma centers lack burn capability).
* **Geospatial Burdens:** Calculated the 100-mile "Failure Zones" using population-weighted county centroids, identifying states where >50% of residents live beyond 100 miles from a burn center (AK, ND, MT, SD, ID, WY, PR).
---

## 🛠️ Tech Stack

| Category | Tools & Resources |
| :--- | :--- |
| **Language** | Python |
| **Libraries** | Pandas, NumPy, Plotly, Folium (Geospatial Visualization) |
| **Data Sources** | NIRD 2023, US Census 2020 (Population Centroids), CDC/ATSDR SVI 2022, USDA RUCC 2023 |

---

## 📂 Repository Structure
* `Burn_Care_ROI_Engine.ipynb`: The core engine for financial modeling and state-level data integration.
* `Visualizations`: Interactive maps showing the "Burn Deserts" and the proposed Tele-Burn Hub network.

---

## 🏆 Hackathon Recognition
Our team (Team 13) was awarded **First Place** for our impactful analysis of geographic disparities. This repository showcases the specific data infrastructure I built to support that winning vision.

> "19 teams. 90+ participants. One shared belief that better data leads to better care. Here's what our winners discovered:
> 
> 🥇 First Place: Team 13 — Josh Spitzer-Resnick, Emmanuel Fle Chea, MPH, Shreya Pramanik, Feifei Li and Lance Killian McDonald."
> — **BData Inc, Official Result Announcement**
