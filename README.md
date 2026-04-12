# Burn Care Equity & Economic Impact Analysis
### 🥇 1st Place Winner: 2026 HeatMap Hackathon (Team 13)
**Official Team Repository:** [efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis](https://github.com/efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis)

This repository contains the independent technical architecture and economic impact models I developed for the **1st Place** winning solution at the 2026 HeatMap Hackathon, hosted by BData and the American Burn Association. 

While the broader team focused on the Composite Vulnerability Index (CVI), **this work provides the specific ROI engine** that quantifies the financial and clinical burden of geographic burn care disparities in the United States.

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
* `Visualizations/`: Interactive maps showing the "Burn Deserts" and the proposed Tele-Burn Hub network.

---

## 🏆 Hackathon Recognition
Our team (Team 13) was awarded **First Place** for our impactful analysis of geographic disparities. This repository showcases the specific data infrastructure I built to support that winning vision.
