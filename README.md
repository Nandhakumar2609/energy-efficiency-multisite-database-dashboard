# Solvay Energy Efficiency Project Database

**End-to-end data analysis project | Production Excellence Team**

Built by **Nandhakumar Chitra Ragupathy** as a portfolio project for the Solvay Stage Analyste Efficacité Énergétique role (Lyon, hybrid).

---

## Project Overview

This repository contains a complete energy efficiency project database for 12 Solvay industrial sites across 5 European countries, covering 49 projects with full techno-economic and regulatory analysis.

### What's inside

| File | Description |
|------|-------------|
| `Solvay_SyntheticData_PowerBI.xlsx` | Clean data tables for Power BI import (4 sheets) |
| `Solvay_EnergyEfficiency_Database.xlsx` | Full Excel workbook with dashboard, calculator, and formatted tables |
| `PowerBI_Dashboard_BuildGuide_Solvay.pdf` | Step-by-step guide to build 5 Power BI dashboards |
| `Solvay_EnergyEfficiency_Presentation.pptx` | 12-slide recruiter presentation |
| `dashboard/index.html` | Interactive HTML dashboard (open in browser) |

---

## Data Model

```
Projects (fact table)
    ├── Site → Sites (dimension)
    ├── Site → Regulatory (dimension)
    └── Technology → Startups (dimension, many-to-many)
```

**Projects table — 49 rows, 16 columns:**
`Project_ID | Site | Country | Business_Unit | Technology | Status | Year | Investment_kEUR | Energy_Savings_MWh | Cost_Savings_kEUR | CO2_Reduction_ktCO2 | Payback_Yrs | NPV_kEUR | IRR_Pct | Priority`

---

## Portfolio Summary

| KPI | Value |
|-----|-------|
| Total Projects | 49 |
| Sites | 12 across France, Belgium, Germany, Italy, Spain, UK |
| Total Investment | 40,631 k€ |
| Annual Energy Savings | 23,765 MWh/yr |
| Annual Cost Savings | 5,512 k€/yr |
| CO2 Reduction | 8.07 ktCO2/yr |
| Completed Projects | 14 (29%) |

---

## 5 Power BI Dashboards

1. **Executive Overview** — Portfolio KPIs, status breakdown, investment by site
2. **Site Performance** — Per-site deep-dive, map, completion rates
3. **Financial Analysis** — IRR, NPV, payback, scatter analysis
4. **Regulatory Compliance** — EU Dir. 2023/1791, ISO 50001/14001, audit tracker
5. **Startup Matchmaking** — Innovation scouting, match scores, recommended actions

---

## Key DAX Measures

```dax
Total Projects = COUNTROWS(Projects)
Total Investment kEUR = SUM(Projects[Investment_kEUR])
Completion Rate = DIVIDE(CALCULATE([Total Projects], Projects[Status]="Completed"), [Total Projects], 0)
Avg IRR Pct = AVERAGE(Projects[IRR_Pct])
Positive NPV = CALCULATE([Total Projects], Projects[NPV_kEUR] > 0)
```

---

## Tools & Technologies

- **Excel Advanced** — Power Query, TCD, INDEX/MATCH, data validation, conditional formatting
- **Power BI** — Star schema, DAX measures, interactive dashboards
- **Python** — pandas, openpyxl, reportlab for data generation and automation
- **SQL (PostgreSQL)** — relational queries and aggregations
- **Regulatory** — EU Directive 2023/1791, ISO 50001, ISO 14001 compliance analysis

---

## Regulatory Coverage

Tracks compliance for all 12 sites across:
- **EU Directive (EU) 2023/1791** — energy efficiency obligations, mandatory audits
- **ISO 50001** — Energy Management Systems
- **ISO 14001** — Environmental Management Systems
- **Energy Audit Schedule** — last audit, next due date, overdue alerts

---

## About the Author

**Nandhakumar Chitra Ragupathy**
MSc Data Science & AI — DSTI School of Engineering, Paris
Bachelor of Engineering — Electrical & Electronics (EEE), Anna University

- Email: nandhakumarragupathy@gmail.com
- Phone: +33 7 45 67 04 24
- LinkedIn: [linkedin.com/in/nandhakumarcr](https://linkedin.com/in/nandhakumarcr)
- GitHub: [github.com/Nandhakumar2609](https://github.com/Nandhakumar2609)
- Location: Paris 94400 | Mobility: Lyon hybrid | Available immediately
