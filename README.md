# Public Commute Experience, Safety & Satisfaction

### A Data-Driven Urban Mobility Analysis using Microsoft Power BI

[![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-F2C811?style=flat&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Primary Data](https://img.shields.io/badge/Data-Primary%20Survey%20(211%20responses)-0A66C2)]()
[![Domain](https://img.shields.io/badge/Domain-Urban%20Mobility%20%26%20Public%20Transport-163F39)]()
[![Status](https://img.shields.io/badge/Status-Completed-success)]()

---

**A multi-page Power BI dashboard and analytical study of real-world public transport experiences across Mumbai and surrounding cities.**

This project analyses how safety perception, affordability, commute duration and satisfaction vary across transport modes, time of day, demographics and day type — and converts those findings into concrete recommendations for urban transport authorities.

---

## 📌 Project Overview

Public transport is the backbone of daily mobility for millions in Indian cities, yet safety perception, crowding and cost remain persistent pain points.  

This project was built to answer:

- Which transport modes feel safest, and under what conditions?
- How do safety ratings change by time of day and weekday vs weekend?
- Who bears the highest expense burden?
- Where should transport authorities prioritise interventions?

**Approach**: Primary survey data → rigorous cleaning & feature engineering in Power Query → DAX measures → interactive multi-page dashboard → data-backed recommendations.

---

## 🗂️ Dashboard Structure (4 Pages)

| Page | Focus | Key Visuals |
|------|-------|-------------|
| **1. Executive Overview** | High-level snapshot | KPI cards (Safety, Expense, Commute Time, High-Risk %), Age distribution, Transport mode usage, Safety by commute duration |
| **2. Safety & Demographic Analysis** | Deep safety exploration | Safety Matrix (Mode × Time of Day), Safety by Time of Day, Safety by Mode, Weekday vs Weekend comparison |
| **3. Strategic Recommendations** | Cost & demographic patterns | Expense vs Commute Time by Mode, Safety Score Distribution by Age Group, Occupation × Expense Category |
| **4. Insights & Recommendations** | Synthesis | Key findings + actionable recommendations for transport planners |

**Interactive elements**: Slicers for Gender, Occupation and City on every page.

---

## 📊 Dataset

| Attribute | Details |
|---------|---------|
| **Source** | Primary data – Google Forms survey + Survey Cycle |
| **Responses** | 211 |
| **Geography** | Primarily Mumbai Metropolitan Region + other Indian cities |
| **Key Fields** | Age group, Gender, Occupation, City, Transport Mode, Time of Day, One-way commute time, Safety Score (1–5), Days/week, Primary safety concern, Daily expense |

### Derived Fields (Power Query)
- Commute Time Category (Short / Medium / Long)
- Expense Category (Low / Medium / High)
- Day Type (Weekday / Weekend)
- Month extracted from commute date
- Frequency Category

---

## 🔧 Technical Implementation

### Power Query Transformations
1. Data type enforcement across all columns  
2. Standardisation of categorical values (city names, occupation, etc.)  
3. Creation of Commute Time Category  
4. Creation of Expense Category  
5. Extraction of Month from commute date  
6. Addition of Day Type (Weekday/Weekend)  
7. Frequency Category derivation  

### Core DAX Measures
- `Total Commuters`
- `Avg Safety Rating`
- `Avg Commute Time`
- `Avg Monthly Expense`
- `% High Safety` (Safety ≥ 4)
- `% Low Safety` / High-Risk % (Safety ≤ 2)
- `Expense per Commuter`

---

## 🔍 Key Findings (Data-Verified)

| Finding | Detail |
|-------|--------|
| **Overall Safety** | Average safety rating = **3.84 / 5**. 10.43% of respondents rated safety ≤ 2. |
| **Safest Mode** | **Metro** leads with 4.42 average safety. Local Train scores lowest at 3.31. |
| **Time of Day Pattern** | Evening (6 PM–Midnight) records the highest average safety (4.09). Early morning (5–9 AM) is the lowest (3.62). |
| **Cost Burden** | Auto / Cab users face significantly higher monthly expenses than Metro, Bus or Train users. |
| **Top Concern** | Overcrowding is the most frequently cited primary safety concern (~27.5%). |
| **Demographic Notes** | Working Professionals (91) and Students (86) form the two largest occupation groups. |

> Note: Written insights in the original report were cross-validated against the raw dataset and corrected for accuracy in this repository.

---

## 💡 Recommendations for Urban Mobility Planners

1. **Strengthen off-peak and early-morning safety infrastructure**  
   Increase lighting, CCTV coverage and visible patrol presence, especially during early morning hours and at Local Train stations.

2. **Address the Auto/Cab cost burden**  
   Explore regulated peak-hour fare frameworks and better last-mile integration with Metro/Bus to reduce over-reliance on high-cost modes.

3. **Prioritise overcrowding mitigation**  
   Peak-hour capacity augmentation and crowd management interventions at high-volume corridors.

4. **Improve weekend service levels**  
   Maintain adequate frequency and staffing on weekends to close the service perception gap.

5. **Targeted support for students and senior citizens**  
   Subsidised monthly passes and better accessibility features at stations.

---

## 🛠️ Tech Stack

- **Microsoft Power BI Desktop** (Dashboard & DAX)
- **Power Query** (Data cleaning & transformation)
- **Excel** (Raw data storage)
- **Google Forms** (Primary data collection)

---

## 📁 Repository Structure

```text
├── Dashboard/
│   └── NashraKhan_2509399_Dashboard.pdf          # Exported 4-page dashboard
├── Dataset/
│   └── Nashra_Khan_2509399_Dataset.xlsx          # Original survey responses
├── Report/
│   └── Nashra_Khan_2509399_Report.docx           # Full project report
├── PBIX/
│   └── NashraKhan_2509399_PowerBi.pbix           # Source Power BI file
└── README.md
