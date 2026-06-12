![header](https://capsule-render.vercel.app/api?type=waving&color=0:8B0000,100:2e86c1&height=220&section=header&text=Is%20Least%20Profitable%20Always%20Unprofitable%3F&fontSize=36&fontColor=ffffff&animation=fadeIn&desc=A%20Tableau%20Investigation%20into%20Retail%20Profit%20Leaks%20%C2%B7%202013–2016&descSize=15&descAlignY=78)

<div align="center">

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)
![Data Analytics](https://img.shields.io/badge/Data%20Analytics-2e86c1?style=for-the-badge&logo=databricks&logoColor=white)

</div>

---

## 📌 Table of Contents

- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Dashboard Features](#dashboard-features)
- [Key Findings](#key-findings)
- [The Verdict](#the-verdict)
- [Business Recommendations](#business-recommendations)
- [Dashboard Preview](#dashboard-preview)

---

## 📖 Introduction

I had the opportunity to complete this project using a **US Retail Superstore Dataset** spanning 2013–2016. The central question driving this analysis is:

> *"Is the least profitable product always truly unprofitable — or is context everything?"*

The dataset covers a retail company selling across three departments — **Furniture, Office Supplies, and Technology** — across multiple US states. My goal was to build an interactive Tableau dashboard that goes beyond surface-level numbers and investigates the *story behind the losses*: which products are genuinely bleeding money, which are recovering, and whether the answer to the title question is yes or no.

---

## 📊 Project Overview

| Aspect | Details |
|---|---|
| **Central Question** | Is the least profitable product always truly unprofitable? |
| **Business Goal** | Identify which loss-making items are genuinely unprofitable vs. which are situationally recoverable |
| **Time Frame** | FY 2013 – FY 2016 |
| **Key Dimensions** | Date → Quarter/Year, Department, Category, Item, US State |
| **Key Facts** | Profit value, Profit trend over time, Geographic profit distribution |
| **Tool Used** | Tableau Desktop / Tableau Public |

---

## ✨ Dashboard Features

The dashboard has two cross-filter actions that make it fully interactive.

**Category Bar Chart → All 3 charts**
Clicking any category filters the Top 10 Items chart, the Map, and the Profit Trend simultaneously — showing data only for that selected category.

**Top 10 Items Chart → Map + Profit Trend**
Clicking any individual item filters the Map and Profit Trend to show only that item's geographic distribution and time-based performance — revealing whether losses are concentrated in specific states or spread broadly.

**Department Dropdown Filter**
Switches the entire dashboard between All, Furniture, Office Supplies, and Technology views.

---

## 🔍 Key Findings

### Top 5 Least Profitable Items — Exact Values

| Rank | Item | Profit | Department |
|---|---|---|---|
| 1 | Okidata Pacemark 4410N Wide Format | **-$39,743** | Technology |
| 2 | Polycom ViewStation ISDN | **-$36,447** | Technology |
| 3 | Epson DFX-8500 Dot Matrix Printer | **-$29,134** | Technology |
| 4 | Global High-Back Leather Tilter, Burgundy | **-$23,238** | Furniture |
| 5 | Lesro Sheffield Collection Coffee Table | **-$14,874** | Furniture |

### What the Trend and Map Reveal Per Item

**Okidata Pacemark 4410N — Profit: -$39,743**
Sold in California, Texas, and Washington only. The profit trend shows a **sharp upward recovery from 2015 Q2 onward**, crossing the trend line and approaching 0K by end of 2016. This is a geographically concentrated loss — not a globally broken product.


<img width="249" height="169" alt="image" src="https://github.com/user-attachments/assets/d2fe3ba1-5efc-41d8-b86a-f6bef6bae755" />


**Polycom ViewStation ISDN — Profit: -$36,447**
Sold in Pacific Northwest and Southeast (Washington, Oregon, Idaho, North Carolina, Alabama). Trend shows **steady improvement from 2013 through mid-2015**, then a dip in late 2015. The improvement phase is real and visible — this product was recovering before something disrupted it.


<img width="249" height="169" alt="image" src="https://github.com/user-attachments/assets/0bb5bf35-a41e-4f38-84c4-042be2602553" />


**Global High-Back Leather Tilter, Burgundy — Profit: -$23,238**
Sold broadly across many US states. Profit trend shows **consistent upward improvement across the full 2013–2016 period**, staying above the trend line for most quarters. Of all items on this list, this one shows the clearest recovery signal.



<img width="232" height="165" alt="image" src="https://github.com/user-attachments/assets/467ff5ba-96a8-4b70-8637-de3a30b5664a" />

Sold in California, Texas, and Wisconsin. Trend shows a **stable loss pattern, then a sharp crash in mid-2016, followed by a recovery back to 0K**. The crash suggests a one-time event (bulk discount or returns spike) rather than a structural problem — but the overall loss is persistent.



<img width="245" height="160" alt="image" src="https://github.com/user-attachments/assets/0d8a68c5-bb6c-45d5-9563-4a851109f1d1" />

**Lesro Sheffield Collection Coffee Table — Profit: -$14,874**
Sold in Washington, Kansas, Texas and Wisconsin. Trend shows a **consistent decline from 2013 through 2016**, worsening over time. This is the most straightforwardly deteriorating item on the list.



<img width="234" height="171" alt="image" src="https://github.com/user-attachments/assets/034dca43-a0db-4b2d-948d-b9b59bcc51f8" />

---

## 🏁 The Verdict

> **Answer: No — least profitable is not always unprofitable. But it depends on the item.**

The data reveals two distinct groups inside the "least profitable" label:

**Group A — Recovering (Do Not Cut Yet)**
Okidata, Polycom, and Global High-Back Leather Tilter all show improving profit trends. Their losses are either geographically concentrated or trending toward zero. Cutting these without further investigation would be premature.

**Group B — Genuinely Declining (Investigate or Exit)**
Lesro Sheffield shows a consistent worsening trend across 4 years. Epson DFX-8500 has a persistent loss with a mid-2016 crash. These need either a pricing fix or discontinuation.

A single profit number is not enough to make the call. The trend direction and geographic concentration change the answer completely.

---

## 💡 Business Recommendations

**1. Do not cut Okidata immediately — fix the geography first**
Loss of -$39,743 but recovering sharply. Audit California and Texas pricing. If a correction was already applied, this product may self-resolve.

**2. Investigate what disrupted Polycom in late 2015**
The improving trend from 2013–2015 was real. A specific event (returns, bulk discount, or pricing error) broke the trajectory. Identifying it could restore profitability.

**3. Monitor Global High-Back Leather Tilter — trend is positive**
At -$23,238 it looks bad. But the 2013–2016 trend is the most consistently improving of all loss-makers. Give it another review period before any exit decision.

**4. Investigate Epson's 2016 crash event**
The sharp mid-2016 dip followed by recovery suggests a one-time event, not a structural problem. Cross-reference with sales records before discontinuing.

**5. Lesro Sheffield — exit or reprice urgently**
The only item showing a consistently worsening trend across all 4 years. No recovery signal anywhere in the data. This one is genuinely and increasingly unprofitable.
0-4995-a1ea-6978dd0cf847" />

