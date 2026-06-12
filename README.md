![header](https://capsule-render.vercel.app/api?type=waving&color=0:8B0000,100:2e86c1&height=220&section=header&text=Is%20Least%20Profitable%20Always%20Unprofitable%3F&fontSize=36&fontColor=ffffff&animation=fadeIn&desc=A%20Tableau%20Investigation%20into%20Retail%20Profit%20Leaks%20%C2%B7%202013–2016&descSize=15&descAlignY=78)

<div align="center">

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data%20Analytics-2e86c1?style=for-the-badge&logo=databricks&logoColor=white)
![Verdict](https://img.shields.io/badge/Verdict-Not%20Always-8B0000?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

</div>

---

## 📌 Table of Contents

- [The Question](#the-question)
- [Project Overview](#project-overview)
- [Dashboard Features](#dashboard-features)
- [Investigation — What The Data Shows](#investigation--what-the-data-shows)
- [The Verdict](#the-verdict)
- [Business Recommendations](#business-recommendations)
- [Data Transformation](#data-transformation)
- [Dashboard Preview](#dashboard-preview)

---

## ❓ The Question

> *"Is the least profitable product always truly unprofitable — or is context everything?"*

This is not just a dashboard. It is an investigation.

A retail company is bleeding money on certain products. The instinct is simple: if something is losing money, cut it. But is that always right? Could a loss-making item today be recovering tomorrow? Could the problem be geographic — not the product itself, but *where* it is being sold?

This Tableau dashboard was built to answer exactly that — by drilling into a US retail dataset spanning **2013 to 2016** across three departments: Furniture, Office Supplies, and Technology.

---

## 📊 Project Overview

| Aspect | Details |
|---|---|
| **Central Question** | Is the least profitable product always truly unprofitable? |
| **Business Goal** | Identify which loss-making items are genuinely dead weight vs. which are recoverable — so management can make data-backed cut/keep/fix decisions |
| **Time Frame** | FY 2013 – FY 2016 |
| **Grain** | One record per product per order |
| **Key Dimensions** | Date → Quarter/Year, Department, Category, Sub-category, Item, US State |
| **Key Facts** | Profit value, Profit trend over time, Geographic profit distribution |
| **Tool Used** | Tableau Desktop / Tableau Public |

---

## ✨ Dashboard Features

The dashboard is fully **interactive and cross-filtered** — every click on one chart updates all others simultaneously.

**Category Bar Chart (left)** — Click any category to filter the entire dashboard: Top 10 Items, Map, and Profit Trend all update to show only that category's data.

**Top 10 Least Profitable Items (right)** — Click any individual item to see exactly which states it was sold in and how its profit trend moved over time. Hover to see exact profit values.

**Profit By State Map** — Color-coded from red (heavy loss) to blue (profit). Reveals geographic concentration of losses — critical for deciding whether a product is globally bad or just regionally mispriced.

**Profit Trend Line** — Shows quarterly profit movement with a dashed forecast/average line. The gap between the trend line and actual line tells you whether an item is improving or deteriorating.

**Department Filter Dropdown** — Switch between All, Furniture, Office Supplies, and Technology to isolate departmental performance.

---

## 🔍 Investigation — What The Data Shows

### Step 1 — Who are the worst offenders?

The Top 10 Least Profitable items across all departments (exact values from dashboard):

| Rank | Item | Profit | Department |
|---|---|---|---|
| 1 | Polycom ViewStation ISDN | **-$36,447** | Technology |
| 2 | Epson DFX-8500 Dot Matrix Printer | **-$29,557** | Technology |
| 3 | Okidata Pacemark 4410N | **-$26,934** | Technology |
| 4 | Global High-Back Leather Tilter, Burgundy | **-$23,238** | Furniture |
| 5 | Tables (category total) | **~-$50,000** | Furniture |

### Step 2 — Are they always unprofitable, or just sometimes?

This is where the title's question gets interesting.

**Okidata Pacemark 4410N** — Loss of -$26,934 overall. But the profit trend chart shows a **sharp upward recovery from 2015 onward**, crossing the trend line and approaching 0K by 2016. Geographically confined to California and Massachusetts only. This item is not globally broken — it is a **geographic pricing problem**, not a product death sentence.

**Polycom ViewStation** — Loss of -$36,447 overall. Trend shows it was **improving steadily from 2013 to mid-2015**, then dropped. Sold in Pacific Northwest states (Washington, Oregon, Idaho). The improvement phase suggests it had potential — the 2015 drop likely signals a discounting or returns event, not inherent unprofitability.

**Epson DFX-8500** — Loss of -$29,557. Sold almost entirely in California and Texas. Trend shows **consistent losses with a dramatic crash in late 2016** — this one shows no recovery. Genuinely and consistently unprofitable.

**Tables (Furniture)** — ~-$50,000 in total losses. Trend fluctuates around 0K with no sustained positive period. Sold broadly across many states. No geographic fix available — the category itself is structurally loss-making.

**Global High-Back Leather Tilter** — Loss of -$23,238 but the **Furniture department's overall trend was improving** from 2013 to 2016. This item is dragging an otherwise recovering department down.

### Step 3 — What about the categories with no least-profit items?

This is equally important. Multiple categories showed **zero items in the Top 10 loss list**:
- Appliances, Paper, Labels, Storage & Organization, Pens & Art Supplies, Scissors & Rulers, Rubber Bands — all in Office Supplies
- Bookcases — in Furniture

These categories are **consistently healthy**. The company's profit engine is intact — the problem is concentrated in specific items, not the business overall.

---

## 🏁 The Verdict

> **Answer: Not always — but in this dataset, mostly yes.**

The data reveals two distinct groups hiding inside the "least profitable" label:

**Group A — Genuinely Unprofitable (Cut or Reprice)**
Epson DFX-8500 and Tables show no recovery trend, no geographic pattern that can be fixed, and consistent losses across the entire time period. These are structural problems.

**Group B — Situationally Unprofitable (Investigate Before Cutting)**
Okidata Pacemark and Polycom ViewStation were showing improving trends before their respective crashes. Their losses are geographically concentrated, not universal. Cutting them without investigation would be a premature decision.

So the answer to "Is Least Profitable Always Unprofitable?" is:

**No — but you need the trend and the geography to know which is which. A single profit number is not enough.**

---

## 💡 Business Recommendations

All recommendations below are based directly on dashboard data — no assumptions added.

**1. Discontinue the Epson DFX-8500 immediately**
Profit: -$29,557. No recovery visible in trend. Concentrated in California and Texas. Geographic restriction or full discontinuation would have immediate P&L impact.

**2. Investigate Okidata Pacemark before cutting**
Profit: -$26,934 overall, but trend was recovering sharply by 2016. Sold only in California and Massachusetts. Check if a pricing correction was already applied — the data suggests it may have been self-correcting.

**3. Exit the Tables category or renegotiate supplier cost**
~-$50,000 total loss with no sustained profitable period in 4 years. The category is sold broadly — this is not a regional fix. Either a supplier renegotiation or full exit is needed.

**4. Review Polycom's 2015 discount/returns event**
The trend was improving before mid-2015. Something happened — likely a bulk discount or returns spike. If that event was one-time, the product may be viable with pricing guardrails.

**5. Protect Telephones & Binders — do not discount these**
These are the top two profit-generating categories. They are currently subsidizing losses elsewhere. Aggressive discounting here would expose the P&L immediately.

---

## 🔄 Data Transformation

The following steps were applied before building the dashboard:

- Structured profit data at Category, Sub-category, and Item level for three departments
- Created calculated fields for profit range (min/max) to power the diverging color legend
- Built cross-filter dashboard actions in Tableau linking all four views
- Applied Department as both a dropdown filter and a drill-down dimension
- Set up state-level geographic roles on the map with profit as the color measure
- Configured the Top 10 filter to show worst-performing items by profit ascending

---

## 📸 Dashboard Preview

**Full Dashboard — All Departments**

![Full Dashboard](dashboard_overview.png)

**Okidata Pacemark — Recovering Trend (supports "Not Always" verdict)**

![Okidata Recovery](okidata_filter.png)

**Polycom ViewStation — Improving then Crashing**

![Polycom Filter](polycom_filter.png)

**Epson DFX-8500 — Genuinely Unprofitable**

![Epson Filter](epson_filter.png)

**Tables Category — Structural Loss**

![Tables Filter](tables_filter.png)

> 💡 **Live Interactive Dashboard:** [View on Tableau Public](#) ← *Replace with your Tableau Public link*

---

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:2e86c1,100:8B0000&height=120&section=footer)

