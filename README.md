# GLP-1 Prescriber White Space Analysis

## Business Problem
GLP-1 drugs (Ozempic, Mounjaro, Trulicity) have seen explosive prescription 
growth, originally approved for Type 2 diabetes but now widely used for weight 
loss. Pharma commercial teams need to understand WHO is prescribing them, WHERE, 
and where the gaps are — because those gaps represent untapped market opportunity.

## What This Project Does
Using 2022 CMS Medicare Part D data, this project analyzes GLP-1 prescribing 
patterns across the US to identify high-value prescribers and commercial 
white spaces.

## Key Findings
- **Family Practice physicians** prescribe more GLP-1s than Endocrinologists
- **Arizona and Illinois** lead in prescription volume
- **Semaglutide (Ozempic/Wegovy)** dominates with 55% of total prescriptions
- **6 Tier 1 high-value prescribers** identified for priority sales targeting

## Limitations
- Data is capped at 5,000 records per drug via the CMS API — large states like 
  CA, NY, and FL are likely underrepresented in geographic findings
- The state-level volume analysis should be interpreted as directional, not absolute
- The specialty finding (Family Practice > Endocrinology) is robust and holds 
  regardless of sample size
- A complete analysis would require the full CMS dataset download (~500MB)

## Tools Used
- **Python** (pandas, requests, matplotlib, seaborn) — data pipeline and analysis
- **SQL** (SQLite) — HCP segmentation and tiering logic
- **Tableau** — interactive commercial intelligence dashboard

## Interactive Dashboard
[View Live Dashboard](https://public.tableau.com/app/profile/prathamesh.lande/viz/GLP1-Prescriber-Commercial-Intelligence-Dashboard/GLP-1CommercialIntelligenceDashboard_)

## Data Sources
- CMS Medicare Part D Prescriber Public Use File (2022)
- Centers for Medicare & Medicaid Services

## Project Structure
```
├── notebooks/
│   ├── 01_data_acquisition.ipynb
│   ├── 02_analysis.ipynb
│   └── 03_sql_analysis.ipynb
├── data/
│   ├── raw/          
│   └── processed/    
├── outputs/          
└── sql/              
```