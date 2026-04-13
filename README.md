### 🧬 Burn Care Equity & Economic Impact Analysis
This project analyzes geographic disparities in burn care access across the U.S., 
identifying critical referral gaps and proposing a telemedicine optimization strategy 
to improve equity and system efficiency.

🥇 1st Place Winner: 2026 HeatMap Hackathon (Team 13)
>"Team 13's submission showcased impactful analysis identifying geographic disparities 
in burn care access, leveraging integrated data to highlight underserved regions and 
inform more equitable resource allocation." — BData Inc, Official Result Announcement

Official Team Repository:[ efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis](efchea1/HeatMap_Burn_2026_Hackathon_Burn_Care_Access_Analysis)

This repository contains the independent technical architecture I developed for the 
1st Place winning solution.

---

🚀 Core Analysis Pillars

**1. Referral Network Optimization**
**The Problem**: Burn care is highly specialized. Delays in transferring patients from 
general trauma centers to ABA-verified burn centers significantly increase mortality 
rates and healthcare costs.

**Our Analysis**: We modeled the "Referral Gap" by identifying Level 1–3 Trauma Centers 
that lack specialized burn capabilities across all 50 states, pinpointing where the 
bottlenecks for acute injuries occur in the national pipeline. Texas emerged as the 
state with the highest volume of such centers, making it a primary target for 
telemedicine intervention.

**2. Telemedicine Feasibility & ROI**
**The Problem**: Maintaining a full-scale burn center is not financially or operationally 
feasible for every region, yet specialized expertise is a universal requirement for 
patient survival.

**Our Analysis**: We identified high-priority trauma centers positioned to serve as 
"Tele-Burn Hubs" using a weighted scoring model (score ≥ 5). By prioritizing these 
hubs in identified burn deserts, we maximize the impact of telemedicine investment. 
California, Texas, and Illinois emerged as the states with the highest number of 
qualifying candidates.

**Scoring Methodology**: 3 pts (trauma center without burn capability) + 2 pts (Level 1 
trauma) + 1.5 pts (Level 2 trauma) + 0.5–1 pt (bed size quartiles).

**3. Equitable Access to Care**
**The Problem**: Socioeconomic factors and geographic isolation create "hidden" disparities 
in burn survival rates that state-level data often masks.

**Our Analysis**: We pivoted from state-level metrics to a high-resolution analysis of 
3,221 U.S. counties using population-weighted centroids (Census 2020). This ensures 
equity priorities are based on actual human density rather than geographic landmass. 
States including **AK, ND, MT, SD, ID, WY, and PR** carry the greatest geographic distance 
burden to ABA-verified care.

---

🚀 Key Technical Contributions

**1. Referral Gap & Systemic Inefficiencies**
I developed a state-level referral gap analysis based on NIRD trauma center data, 
computing the number of L1–L3 trauma centers lacking burn capability for every state. 
By mapping trauma center distribution against ABA-verified burn centers, the analysis 
establishes a data-driven foundation for prioritizing telemedicine hub activation.

**2. Telemedicine ROI & Spoke Mapping**
I engineered the logic to identify "Tele-Burn Hub" candidates by scoring trauma centers 
based on trauma level, bed size, and absence of burn capability. The model surfaces 
high-priority sites (score ≥ 5) nationally, with California, Texas, and Illinois 
ranking as the top three states by candidate volume — making these the primary targets 
for telemedicine network implementation.

**3. Geospatial Equity Engineering**
- **Distance Burden**: Calculated population-weighted Haversine distances from 3,221 U.S. 
  county centroids (Census 2020) to the nearest burn center, identifying states where 
  the population-weighted distance burden is highest (AK, ND, MT, SD, ID, WY, PR).
- **ABA Quality Gap**: Distance to ABA-verified care is tracked separately, revealing 
  cases where a state has a burn center but no ABA-verified facility within a 
  clinically meaningful distance (e.g., Hawaii: 0 miles to any burn center, 2,385 
  miles to the nearest ABA-verified center).
- **Vulnerability Integration**: Integrated CDC SVI 2022 variables — poverty (EP_POV150), 
  minority status (EP_MINRTY), disability (EP_DISABL), and vehicle access (EP_NOVEH) — 
  into the state-level equity framework.

**4. Economic Impact Modeling**
Using Huang et al. (2021), Murray et al. (2019), and Ivanko et al. (2024), the model 
projects state-level avoidable hospitalization costs driven by burn under-referral 
(66% under-referral rate × 6.9 excess LOS days × $3,500/day). States with zero burn 
centers are assigned a 90% under-referral penalty. National totals are computed at 
runtime from the NIRD + Census dataset.

Note: Cost projections reflect avoidable excess hospitalization days only. An earlier 
infection cost multiplier was removed from the model due to lack of a peer-reviewed 
citation.

---

📚 Research Bibliography
- NIRD Framework: Lovick et al., Burns (2024)
- Economic Burden: Ivanko et al., J Burn Care Res (2024)
- Under-Referral Rate: Huang et al. (2021)
- Excess LOS: Murray et al. (2019)

---

🛠️ Tech Stack
Language: Python
Libraries: Pandas, NumPy, Plotly, Folium (Geospatial Visualization)
Data Sources: NIRD 2023, US Census 2020 (Population Centroids), CDC/ATSDR SVI 2022, 
              USDA RUCC 2023

📂 Repository Structure
- Burn_Care_ROI_Engine.ipynb: Core engine for data integration, referral gap analysis, 
  telemedicine scoring, distance burden computation, and economic impact modeling.
- Visualizations: Interactive maps showing burn deserts and the proposed Tele-Burn Hub 
  network.  [https://fayfaymn.github.io/Burn-Care-Equity-Analysis-ROI/](url)
