# Domain Expertise: Burn Care Systems Engineering

This repository integrates structural data from the **National Injury Resource Database (NIRD)** with public health equity frameworks to address the three core challenges defined by the **HeatMap Hackathon**.

---

## 🔬 Core Analysis Pillars

### 1. Referral Network Optimization
**The Problem:** Burn care is highly specialized. Delays in transferring patients from general trauma centers to ABA-verified burn centers significantly increase mortality rates and healthcare costs.

* **Key Insight:** According to *Use_Case_Publications.docx*, palliative care is often under-utilized in burn centers (only **9.6%** referral rate). This indicates a critical need for clearer referral criteria that extend beyond "end-of-life" scenarios to include complex symptom management.
* **Our Analysis:** We modeled the **"Referral Gap"** by identifying Level 1–3 Trauma Centers that lack specialized burn capabilities, pinpointing exactly where the bottlenecks for acute injuries occur in the national pipeline.

### 2. Telemedicine Feasibility & ROI
**The Problem:** Maintaining a full-scale burn center is not financially or operationally feasible for every region, yet specialized expertise is a universal requirement for patient survival.

* **Key Insight:** As noted in the *Data_Mapping_Document.docx*, effective telemedicine deployment requires a mechanical link between hospital infrastructure (bed capacity) and geographic demand.
* **Our Analysis:** We identified **351 specific trauma centers** positioned to serve as "Tele-Burn Hubs." By prioritizing these hubs in identified "burn deserts," we maximize the **Return on Investment (ROI)** for healthcare systems while drastically reducing the economic burden of air-transfers.

### 3. Equitable Access to Care
**The Problem:** Socioeconomic factors and geographic isolation create "hidden" disparities in burn survival rates that state-level data often masks.

* **Key Insight:** Data from the *County-level one page Overview.docx* shows that Social Vulnerability (SVI) creates a **2.1x distance burden**. A stark example is Hawaii, where residents may be 47 miles from a general hospital but **2,385 miles** from ABA-verified expertise.
* **Our Analysis:** We pivoted from state-level metrics to a high-resolution analysis of **3,135 U.S. counties** using **population-weighted centroids**. This ensures equity priorities are based on actual human density rather than geographic landmass.

---

## 📚 Research Bibliography & Resources

* **The NIRD Framework:** Based on *Development of the National Injury Resource Database* (Lovick et al., 2023), validating the landscape of 135 Burn Centers vs. 617 Trauma Centers.
* **Economic Burden:** Grounded in *The Burden of Burns: An Analysis of Public Health Measures* (Ivanko et al., 2024), focusing on addressing the ambiguity of societal burn burden.
* **Regional Success Models:** Referencing the **Maine regionalized system**, which demonstrated that mortality benchmarks can be met in rural populations through tiered, selective referral rather than universal transfer.

---

## ⚖️ Evaluation Alignment

Our methodology is specifically engineered to meet the **Judge Evaluation Form** criteria:

* **Clinical/Business Alignment:** Directly solves the "Referral Network" and "Equitable Access" use cases.
* **Analytic Rigor:** Implementation of **sensitivity analysis across 5 weight schemes** to ensure statistical robustness and eliminate weighting bias.
* **Actionability:** Moving beyond theory to provide a clear, data-driven roadmap for **Tele-Burn hub deployment**.
