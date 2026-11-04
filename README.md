# california-public-health-equity-case-study
Google Data Analytics Certificate Capstone analyzing California county-level mortality and preventative care disparities (2021–2023).

# Google Data Analytics Capstone: California Public Health Equity Case Study (2021–2023)

**Author:** Atar Cheema  
**Tools Used:** Google Sheets, Tableau Public  

---

## 1. ASK Phase

### Business Task
To analyze publicly available California county-level public health data from 2021–2023 to identify geographic differences in coronary heart disease (CHD) death rates, diabetes death rates, and early prenatal care percentages. This analysis will support evidence-based resource planning and improve performance monitoring across California counties without directly assessing existing program expenditures.

### Stakeholders
- **Primary:** California public health officials and program administrators.
- **Secondary:** County public health departments and local program managers.

### Analysis Questions
1. **Geographic Variance of Cardiovascular Mortality:** How do age-adjusted Coronary Heart Disease (CHD) mortality rates vary geographically across California counties during the 2021–2023 reporting period?
2. **Geographic Variance of Metabolic Mortality:** How do age-adjusted Diabetes Mellitus mortality rates vary across California jurisdictions during the 2021–2023 timeline?
3. **Assessment of Preventative Care Access:** What geographic disparities exist in the percentage of live births receiving first-trimester prenatal care across California during 2021–2023?
4. **High-Burden Jurisdictions & Resource Modeling:** Which specific California counties exhibit a critical dual-burden of high chronic mortality (CHD/Diabetes) alongside deficient preventative care access, and what supplementary datasets are required to optimize regional public health resource allocation?

---

## 2. PREPARE Phase

### Data Source Information
- **Dataset Name:** California County Health Status Profiles (2021–2023).
- **Availability:** Publicly available health data provided by the state health department.
- **Data Integrity (ROCCC Assessment):**
  - **Reliable:** Yes, sourced from official government vital statistics.
  - **Original:** Yes, primary public health surveillance data.
  - **Comprehensive:** Contains stable age-adjusted rates and tracking indicators for all 58 California counties.
  - **Current:** Focuses on the recent 2021–2023 period.
  - **Cited:** Officially documented and open-source.
* **Replication Dataset:** The fully processed, filtered source data is available directly within this repository as `California_Public_Health_Clean_Data.csv`.

### Data Privacy & Security
The dataset consists entirely of aggregated, de-identified county-level statistics. There is zero risk of exposing Personally Identifiable Information (PII).

---

## 3. PROCESS Phase

### Tool Selection
- **Google Sheets:** Chosen for initial data ingestion, filtering, schema validation, and structural sorting.
- **Tableau Public:** Chosen for advanced geographical mapping, data synthesis, and interactive stakeholder dashboards.

### Data Cleaning Log
1. **Tabular Hierarchy and Formatting:** Standardized structural formatting by right-aligning all quantitative metrics (Age-Adjusted Mortality Rates and Prenatal Percentages) to align decimal points for rapid scannability. Maintained left-alignment for categorical text fields and qualitative identifiers (County Name, County ID, and Publication Year) to treat them strictly as descriptive labels.
2. **Structural Trimming:** Removed unneeded summary metadata fields, empty separator rows, and disabled default spreadsheet Grand Totals to prevent skewed averages.
3. **Missing Value Management:** Isolated empty data cells using conditional filters to verify whether blanks represented data suppression (due to low case counts) or missing metrics.
4. **Field Filtering:** Hid unused tracking fields to isolate key indicators: CHD death rates, diabetes death rates, and first-trimester prenatal care percentages.

---

## 4. ANALYZE Phase

### 1. Geographic Variance of Cardiovascular Mortality
The age-adjusted Coronary Heart Disease (CHD) mortality data reveals distinct geographic groupings across California jurisdictions:
- **High-Burden Outliers:** Lake, Kern, Amador, Glenn, and Yuba counties exhibit the highest age-adjusted CHD death rates in the state. These jurisdictions are primarily located within inland, northern, or Central Valley regions, highlighting geographic corridors that may benefit from targeted cardiovascular health evaluations.
- **Low-Burden Outliers:** Monterey, Santa Cruz, Mono, San Benito, and Alpine counties record the lowest cardiovascular mortality. These counties are predominantly located along coastal lines or specific mountain corridors, establishing a baseline for low-burden comparison.

### 2. Geographic Variance of Metabolic Mortality
Diabetes Mellitus mortality patterns show distinct regional distributions, with specific inland and agricultural regions exhibiting elevated rates:
- **High-Burden Outliers:** Del Norte, Kern, Merced, San Benito, and San Bernardino represent the highest age-adjusted diabetes death rates. Kern County emerges as an acute outlier across both cardiovascular and metabolic categories, signaling a compounding public health trend. The concentration of high rates in Central Valley and Inland Empire regions points to regional metabolic risk concentrations.
- **Low-Burden Outliers:** Calaveras, Nevada, Marin, Mono, and Alpine exhibit the lowest metabolic mortality, establishing the baseline for low-burden metropolitan and mountain comparisons.

### 3. Assessment of Preventative Care Access
First-trimester prenatal care percentages expose a clear gap between major metropolitan hubs and rural or border jurisdictions:
- **High-Access Outliers:** San Mateo, Orange, San Francisco, Santa Clara, and Alameda report the highest percentages of early prenatal care utilization. These represent major coastal and metropolitan centers in northern and southern California.
- **Low-Access Outliers:** Alpine, Tehama, Trinity, Imperial, and Modoc counties record the lowest percentages of early prenatal care. This grouping highlights a concentration of low preventative care access within northern mountain regions and southern border zones, identifying potential geographic barriers to early maternal care penetration.

### 4. High-Burden Jurisdictions & Critical Data Anomalies
Cross-indicator synthesis reveals specific regions experiencing a critical dual-burden, alongside a unique statistical outlier that dictates further investigation:
- **The Kern County Dual-Burden:** Kern County stands out as a critical priority area in California, ranking simultaneously in the top tiers for both CHD and Diabetes Mellitus mortality. This chronic disease clustering identifies a clear geographic focus for performance monitoring.
- **The Alpine County Paradox:** Alpine County presents a unique public health profile. It ranks among the best in the state for low cardiovascular and metabolic mortality, yet ranks as the absolute lowest in first-trimester prenatal care access. This striking divergence demonstrates that low chronic disease mortality does not automatically correlate with high preventative healthcare access. It highlights a critical area where further evaluation is needed to determine if the trend is driven by data artifacts related to small sample sizes or the utilization of out-of-county healthcare facilities.

<img width="1634" height="340" alt="Screenshot 2026-11-03 at 2 07 08 PM" src="https://github.com/user-attachments/assets/051c258c-6a61-43f4-ab5f-9cdffc56e5ed" />

### High-Burden Priority Jurisdictions (2021–2023 Summary Table)

| County | Reporting Timeline | Age-Adjusted CHD Death Rate | Age-Adjusted Diabetes Death Rate | First-Trimester Prenatal Care |
| :--- | :--- | :--- | :--- | :--- |
| **Kern** | 2021–2023 | *High Outlier* | *High Outlier* | Intermediate Baseline |
| **Lake** | 2021–2023 | *High Outlier* | Intermediate Baseline | Intermediate Baseline |
| **Del Norte** | 2021–2023 | Intermediate Baseline | *High Outlier* | Intermediate Baseline |
| **Alpine** | 2021–2023 | *Low Outlier* | *Low Outlier* | **Lowest Outlier** |
| **Imperial** | 2021–2023 | Intermediate Baseline | Intermediate Baseline | *Low Outlier* |

---

## 5. SHARE Phase
<img width="1657" height="345" alt="Screenshot 2026-11-03 at 2 49 05 PM" src="https://github.com/user-attachments/assets/4e539650-35dc-43b1-bcce-0effa29932f6" />

### Visualization Strategy
Data findings were migrated from Google Sheets into Tableau Public to construct the interactive "Mapping Health Equity" dashboard. The visual architecture was optimized to allow health administrators and state stakeholders to rapidly isolate performance gaps and evaluate regional disparities.
- **County Rankings Chart:** A sorted horizontal bar chart was deployed as the primary comparative asset, allowing stakeholders to immediately scan and identify upper- and lower-bound outlier jurisdictions without visual fatigue.
- **Geographic Mapping:** Independent county-level spatial maps were generated to visualize the regional distribution of cardiovascular mortality, metabolic mortality, and preventative prenatal care access across California.

### Strategic Color Palette Architecture & Accessibility
To prevent data confusion and ensure clear visual separation between distinct health indicators, independent color schemes were utilized across the dashboard maps:
- **Diabetes Mellitus Map (Orange-Blue):** An Orange-Blue diverging scheme was selected to map metabolic mortality. This combination is universally colorblind-friendly, ensuring high contrast and clean legibility for stakeholders with red-green color vision deficiencies.
- **Coronary Heart Disease Map (Red-Blue):** A traditional Red-Blue diverging scheme was utilized for cardiovascular mortality. This leverages standard institutional familiarity, where red universally signals acute clinical risk or high mortality rates.
- **Functional Differentiation:** Utilizing entirely different color schemes for the metabolic and cardiovascular maps allows stakeholders to instantly distinguish between the two health conditions, minimizing cognitive load when viewing the dashboard components concurrently.
### Geocoding Limitations & Technical Constraints
During the spatial map construction within Tableau Public, a native geocoding limitation was identified regarding specific jurisdiction profiles:
* **Spatial Mapping Omissions:** Due to geographic boundary discrepancies or sample suppression filters within Tableau's native map layer, certain low-population or remote California counties (such as Alpine) failed to render polygon markers on the filled geographic maps, despite multiple troubleshooting iterations (including utilizing full state/county location tuples).
* **Analytical Safeguards:** To protect data integrity and prevent structural data loss, the data values for these omitted jurisdictions were fully preserved and prioritized within the sorted horizontal **County Rankings bar chart** and the **High-Burden Priority Summary Table**. Stakeholders are advised to cross-reference the geographic maps with the tabular rankings to ensure complete statewide coverage.


**Interactive Tableau Dashboard:**  
[View Tableau Public Dashboard](https://public.tableau.com/views/California_Health_Equity_Case_Study/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

## 6. ACT Phase

### Evidence-Based Recommendations
- **Geographically Targeted Resource Modeling**
  - Prioritize regional health screening deployments and mobile healthcare clinics within the specific high-burden hubs identified in the master dataset, with immediate focus on the critical chronic disease dual-burden observed in Kern County.
  - Direct localized maternal health outreach and prenatal support programs to the remote northern mountain corridors (Tehama, Trinity, Modoc) and southern border zones (Imperial) exhibiting the lowest percentages of early prenatal care utilization.
- **Targeted Performance Monitoring & Diagnostic Evaluation**
  - Launch a targeted public health evaluation in Alpine County to investigate the localized structural factors or cross-border medical dependencies driving its unique statistical paradox of low chronic disease mortality alongside the state's lowest first-trimester prenatal care access.
  - Establish standardized quarterly state-to-county data pipelines to monitor real-time shifts in prenatal care utilization, moving away from multi-year aggregate reporting timelines to enable rapid intervention deployment.
- **Administrative Data Integration to Address Core Gaps**
  - Formally acquire supplementary localized data assets—specifically county-level public health expenditures, clinical program staffing volumes, and direct facility capacities.
  - Cross-reference these missing resource indicators with the established outcome profiles to systematically evaluate resource distribution efficiency, moving the operational model from passive performance monitoring to true evidence-based resource planning.


