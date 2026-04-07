# 🏥 NHS Referral-To-Treatment(RTT) Performance & Capacity Tracker

![RTT Performance & Capacity Tracker Main](/Screenshots/NHS%20RTT%20Performance_Capacity%20Tracker.png)


## 📌 Project Overview
The National Health Service (NHS) aims to start treatment for patients within 18 weeks of referral. This end-to-end Power BI application was developed to track Referral to Treatment (RTT) performance, identify systemic bottlenecks across medical specialties, and highlight hospital trusts operating critically below national benchmarks.

Unlike standard reporting, this dashboard is designed with **Enterprise UI/UX principles** and advanced **DAX statistical controls** to ensure executives are acting on statistically significant operational data rather than mathematical anomalies.

## 🛠️ Technical Stack
* **Data Engine & Visualization:** Power BI
* **Data Modeling & ETL:** Power Query
* **Calculations:** Advanced DAX (Context transition, dynamic benchmarking, referential integrity)
* **UI/UX Design:** Figma (Custom canvas backgrounds, exact NHS branding guidelines `#005EB8`)

## 🚀 Key Methodologies & Advanced Logic

### 1. Controlling for "Small Denominator" Statistical Anomalies
**The Problem:** Standard ranking by "Breach Rate %" caused tiny clinics with 1 patient (100% breach rate) to rank worse than massive hospital trusts failing 90,000 patients (51% breach rate), rendering the dashboard operationally useless for executives.

**The Solution:** Implemented dynamic DAX logic using `RANKX` and `FILTER` to establish a Minimum Volume Threshold, ensuring only trusts with statistically significant waitlists (>1,000 patients) or ranking by absolute volume are flagged for executive review.


### 2. Progressive Disclosure & App-Like Navigation
To prevent cognitive overload, the dashboard utilizes the Progressive Disclosure UX principle.

Zone 1 (Macro): High-level KPIs and top 5 worst-offending trusts using Top N visual filtering.

Zone 2 (Micro): Analysts can drill through to a hidden "Full Leaderboard" matrix via seamless page navigation.

### 3. Enterprise Formatting & Data Cleanliness
Null Handling: Executed Power Query transformations to replace null waitlist values with 0 to prevent DAX calculation breaks, while aggressively filtering orphaned rows (missing hospital names) to maintain referential integrity.

Cognitive Load Reduction: Eliminated vertical scrollbars via dynamic scaling, disabled redundant Grand Totals, and applied strict data alignment standards (Right-aligned numbers/percentages, Left-aligned categories) for rapid visual scanning.

## 🗂️ Data Structure (Star Schema)
Fact_Waitlist: Contains transactional data of patient volumes, wait bands, and 52+ week breach flags.

Dim_Provider: Dimension table for Hospital Trusts.

Dim_Specialty: Dimension table for Medical Treatment Functions.

## 🤝 Let's Connect
If you're a recruiter or hiring manager, I'd love to chat about how I can bring this level of data modeling and UX design to your team.

[LinkedIn](https://www.linkedin.com/in/vani-basavaraj-gourish/)
