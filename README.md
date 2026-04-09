# 1. Project Title and Decision Statement
Strategic growth analysis for Halifax International Airport Authority(HIAA): Evaluating investment tradeoffs between seasonal European tourism and year-round flights to the US.

### Decision Statement
*Should the Senior Leadership Team of the Halifax International Airport Authority (HIAA) prioritize incentive funding for seasonal European expansion to boost high-value tourism, or focus on year-round transborder connectivity to ensure regional economic stability?*

# 2. Executive Summary

Following a period of significant expansion, Halifax Stanfield (YHZ) recently reached a milestone of **4.1 million annual passengers**, signaling a robust new growth phase for Atlantic Canada’s primary gateway (HIAA, 2026). This momentum is driven by two distinct market trends: a **19.3% surge** in international travelers, fueled by seasonal transatlantic expansion, and an **8.5% increase** in transborder (U.S.) traffic, supported by the entry of new year-round jet services (HIAA, 2026; Tourism Nova Scotia, 2025).

The airport’s Senior Leadership Team faces a recurring strategic choice regarding the allocation of limited air service incentive funding for future growth phases. While high-capacity seasonal flights to Europe generate massive economic impact—with air travelers spending an average of **$1,224 per person** they can lead to underutilized infrastructure during off-peak months (Tourism Nova Scotia, 2024). Conversely, year-round transborder routes offer greater economic stability and consistent local employment but typically operate on lower immediate margins per passenger (HIAA, 2025).

This project analyzes which investment strategy best supports Nova Scotia’s long-term economic resilience. By evaluating the trade-offs between seasonal "value" and year-round "volume," this analysis provides a data-driven framework to help HIAA leadership maximize the airport’s regional economic contribution in upcoming strategic cycles.

# 3. Table of Contents
1. [Project Title and Decision Statement](#1-project-title-and-decision-statement)
2. [Executive Summary](#2-executive-summary)
3. [Table of Contents](#3-table-of-contents)
4. [Background](#4-background)
5. [Data Sources](#5-data-sources)
6. [Exploratory Findings](#6-exploratory-findings)
7. [System Dynamics](#7-system-dynamics)
8. [Analysis](#8-analysis)
9. [Recommendations](#9-recommendations)
10. [Limitations and Future Work](#10-limitations-and-future-work)
11. [References](#11-references)

# 4. Background
### Why This Decision Matters: The Economic Stakes

Halifax Stanfield International Airport (YHZ) serves as the primary economic gateway for Atlantic Canada and a critical engine for regional prosperity. Recently, the airport reached a landmark milestone of 4.1 million annual passengers, signaling the beginning of a robust new growth phase for the region. For the Senior Leadership Team (SLT) of the Halifax International Airport Authority (HIAA), this growth presents a complex management challenge. The stakes are exceptionally high because air service development is not a passive occurrence; it requires the strategic allocation of "incentive funding"—which includes financial subsidies, marketing support, or landing fee waivers—to attract and retain airlines in a competitive global market.

Because these financial resources are finite, the SLT must choose where to place its bets. A strategic misstep in this allocation could lead to significant negative consequences, such as underutilized infrastructure during off-peak months or a lack of the consistent, year-round connectivity that Nova Scotian businesses require for long-term stability. This decision effectively determines the airport’s role in the regional economy for the next strategic cycle.

### Tensions and Trade-offs: The Difficulty of the Choice

The core difficulty of this decision lies in a fundamental trade-off between seasonal "value" and year-round "volume." This choice is non-obvious because both paths offer distinct advantages and significant risks.

On one hand, prioritizing seasonal European expansion targets high-capacity transatlantic flights during the peak summer months. These routes are incredibly lucrative for the province, as international air travelers spend an average of $1,224 per person, providing a massive seasonal injection into the hospitality and tourism sectors. However, this model creates "peak-load" issues. The airport must maintain infrastructure and staffing levels capable of handling these summer surges, which then sit underutilized during the winter months, leading to operational inefficiencies and seasonal employment volatility.

On the other hand, focusing on year-round transborder (U.S.) connectivity provides the economic "connective tissue" for the region. These routes support consistent business travel, specialized cargo logistics, and reliable regional employment that does not disappear when the leaves change. While these flights offer greater regional economic resilience, they typically operate on lower immediate profit margins per passenger compared to high-spending European "bucket list" tourism. The SLT is forced to navigate the tension between a short-term, high-value tourism spike and long-term, steady-state economic stability.

### Context: Previous Approaches and Current Challenges

Historically, HIAA has pursued a diversified "all-of-the-above" strategy, attempting to grow all sectors simultaneously. However, in the post-2025 landscape, this approach is becoming unsustainable. While international travel has surged by 19.3% and transborder traffic has increased by 8.5%, the airport is reaching its physical capacity limits during peak periods. With incentive funds limited and infrastructure nearing its maximum summer load, the SLT can no longer afford to be everything to everyone. They must now decide whether to double down on the high-value summer market or pivot their investment to secure the year-round hub access that keeps the Nova Scotian economy resilient throughout the entire year.

---
# 5. Data Sources

This directory contains the raw data files required for the HIAA Strategic Growth Analysis. These datasets provide the evidence for the "Value vs. Volume" trade-off between seasonal European tourism and year-round transborder connectivity.

---

#### 1. Monthly Screened Passenger Data (2019-2026).csv
* **Source:** Statistics Canada. Table 23-10-0312-01 Screened passenger traffic at the largest airports in Canada.
* **Date Accessed:** April 6, 2026
* **Usage Restrictions:** Statistics Canada Open Licence
* **Description:** This dataset provides monthly counts of screened passengers at Halifax Stanfield (YHZ), broken down by sector (Domestic, Transborder, and Other International). It is used to analyze growth trends and seasonality patterns.

#### 2. Visitor Spending Data.csv
* **Source:** Statistics Canada. Table 24-10-0066-01 Visits, nights and spending for visitors to Canada by geography of visit, residency and mode of transport.
* **Date Accessed:** April 6, 2026
* **Usage Restrictions:** Statistics Canada Open Licence
* **Description:** Quarterly data detailing the total and average spending of non-resident visitors to Nova Scotia. This allows for a comparison between the economic "Value" of Overseas (European) vs. U.S. visitors arriving by air.

#### 3. Tourism Nova Scotia Visitation (By Origin and Mode).csv
* **Source:** Open Data Nova Scotia / Tourism Nova Scotia.
* **Date Accessed:** April 6, 2026
* **Usage Restrictions:** Open Government Licence - Nova Scotia
* **Description:** Monthly visitation data for Nova Scotia categorized by origin (e.g., UK, Germany, USA regions) and mode of entry. This data is filtered for "Air" arrivals to isolate passengers relevant to HIAA operations.

#### 4. Halifax Employment Data.csv
* **Source:** Statistics Canada. Table 14-10-0466-01 Employment characteristics by economic region, annual.
* **Date Accessed:** April 6, 2026
* **Usage Restrictions:** Statistics Canada Open Licence
* **Description:** Annual employment statistics for the Halifax economic region. This dataset provides the evidence for the "Regional Economic Stability" variable in the Causal Loop Diagram (CLD).

# 6. Exploratory Findings

## Project Overview
This project analyzes the recovery and trends within the aviation and tourism sectors, specifically focusing on the relationship between industry employment, passenger volume, and international visitor spending.

---

## Visualizations & Insights

### 1. Employment vs. Passenger Traffic Trends
![Employment vs Passenger Traffic](img/Viz-Employment-Passgenger.png)

**Insight:** 
This visualization tracks the correlation between the industry's labor force and actual passenger volume. Both metrics saw a significant decline beginning in 2020,due to the Covid-19 Pandemic. While Employment Count (blue) has shown a steady, linear recovery through 2025, Passenger Count (orange) exhibited a more aggressive surge in 2024 and 2025. The sharp decline shown in 2026 likely reflects year-to-date data rather than a projected collapse. This data focuses on the Halifax region of Nova Scotia. It would be useful to see the monthly metrics for seasonality of employment, however those metrics were unavailable in the dataset.

### 2. Visitor Spending Patterns
![Spending Data](img/Viz-Spending-Data.png) 

**Insight:** This bar chart highlights the economic impact of visitors based on their area of residence. After a substantial data gap in 2021 and 2022 (largely due to travel restrictions and reporting exclusions), visitor spending rebounded strongly in 2023. The data indicates that spending levels in the post-recovery period have remained consistent with, or exceeded, pre-pandemic levels from 2019, showing high resilience in travel budgets.

### 3. Passenger Seasonality Heatmap
![Seasonality Heatmap](img/Viz-Seasonality-Heatmap.png) 

**Insight:** The heatmap provides a granular look at when travel peak periods occur. Quarter 3 (Q3) consistently emerges as the high-traffic season, indicated by the warmer red and orange tones. The "cool" green block across all quarters in 2021 illustrates the total cessation of standard travel patterns. By 2024 and 2025, we see a return to intense seasonality, with Q3 remaining the most critical period for passenger volume.

### 4. Visitor Origin Analysis
![Visitor Origin](img/Viz-Visitor-Origin.png)

**Insight:** This packed bubble chart illustrates the primary source markets for tourism. The United States represents the largest single share of visitors by a significant margin. Outside of North America, the United Kingdom, Germany, and Other European countries constitute the core international demographic. This distribution suggests that marketing and infrastructure efforts are most heavily influenced by the needs and trends of the American traveler.

---

# 7. Systems Dynamics 

### Initial CLD Diagram 

![Causal Loop Diagram](img/cld-draft.png)

---

# 8. Analysis

## Systems Analysis of Nova Scotia Tourism Recovery
### 1. System Archetype Identification 

**Chosen Archetype:** Growth and Underinvestment 

In the context of Nova Scotia’s post-pandemic recovery, the "Growth and Underinvestment" archetype explains the tension between rising visitor numbers and a constrained service-sector workforce.

**The Growth Loop:** As passenger traffic recovered (the "orange line" in my dashboard), tourism revenue and demand increased, creating a reinforcing loop for economic growth.

**The Constraint:** This growth is approaching a limit defined by labor capacity. My data shows that while passenger counts have surged back toward 400K annually, employment has remained relatively flat at around 800 (000s).

**The Underinvestment:** If the decision-maker (e.g., Tourism Nova Scotia) focuses only on marketing to increase demand without addressing the "sturdy but flat" employment baseline, the quality of the visitor experience will eventually decline, creating a self-limiting loop.

**Evidence from Data**

My "Employment vs. Passengers" dual-axis chart provides the primary evidence. The "orange heartbeat" of travel shows a volatile but strong upward trajectory, while the "blue line" of employment shows a much slower, inelastic growth. This gap indicates that the system is trying to handle pre-pandemic levels of demand with a workforce that has not scaled at the same rate.

### 2. Scenario Narratives 

**Scenario 1:** Status Quo (Continued Demand Focus) 

In this scenario, the decision-maker continues to prioritize high-volume marketing to attract US and overseas residents. Over the next 5-10 years, the seasonality peaks in Q3 will continue to intensify. However, because the employment baseline remains stagnant, service quality in key hubs like Halifax and Antigonish begins to erode. This triggers a "Limits to Growth" loop where negative word-of-mouth regarding wait times and service availability eventually offsets the marketing gains, leading to a plateau in visitor spending by 2030.

**Scenario 2:** Intervention A (Labor-Led Investment) 

The decision-maker shifts focus toward workforce retention and service-sector training programs. Quantitatively, this aim is to move the "blue line" of employment from its 800 baseline toward 900 by 2028. By stabilizing the labor supply, the province can handle higher passenger volumes during the Q3 peak without a drop in service quality. This strengthens the reinforcing loop of visitor satisfaction, leading to a projected 15% increase in spending from "high-roller" overseas residents who value premium service.

**Scenario 3:** Intervention B (Seasonality Smoothing) 

Instead of just growing the workforce, the decision-maker intervenes to "smooth" the seasonality heatmap. By investing in "off-season" (Q1 and Q4) tourism products—such as winter festivals or business conventions—demand is redistributed across the year. This reduces the "Escalation" pressure on the workforce during the summer. The system becomes more stable, allowing for year-round employment rather than seasonal churn, which naturally improves long-term workforce expertise and provincial tax revenue.

### 3. Leverage Point Analysis 

The most promising leverage point is shifting the goal of the system from "Volume" to "Value and Stability." 

**Why high impact:** Focusing on seasonal smoothing (Intervention B) offers high impact because it addresses the core "bottleneck" (the Q3 peak) without requiring an impossible surge in the total workforce.

**Feedback loops affected:** This intervention weakens the "Limits to Growth" loop by reducing the peak-season strain on resources.

**Risks:** The primary risk is resistance from the private sector, which is traditionally optimized for the summer rush.

### 4. Implications for the Decision 

My analysis reveals that Nova Scotia's tourism recovery is robust but physically limited by its labor supply. The evidence shows that while we can successfully bring passengers back to the province, we are not scaling our service capacity at the same rate.

Based on this, the option to purely increase marketing to the "Middle Atlantic" or "UK" markets looks less promising unless paired with labor support. The most promising path is to invest in off-season infrastructure to make tourism employment a year-round, sustainable career. A key uncertainty remains regarding whether the "sturdy" employment baseline is due to increased automation or a genuine shortage of workers. My recommendation in Milestone 4 will focus on a dual strategy of targeted high-value marketing and seasonal redistribution to ensure the system does not "crash" against its labor limits.

---

# 9. Recommendations 

---

# 10. Limitations and Future Work 


---

## 11. References

Halifax International Airport Authority. (2026). *Annual Passenger Statistics and Regional Growth Outlook*. HIAA Newsroom. 

Halifax International Airport Authority. (2025). *Strategic Plan: Connecting Nova Scotia to the World*. HIAA Corporate Publications.

Tourism Nova Scotia. (2025). *Tourism Performance Indicators: Annual Visitation Report*. Government of Nova Scotia.

Tourism Nova Scotia. (2024). *Visitor Travel Survey: Air Traveler Spend and Behavior Analysis*. Government of Nova Scotia.
