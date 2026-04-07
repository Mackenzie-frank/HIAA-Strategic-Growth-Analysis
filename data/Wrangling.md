# Data Wrangling Report: HIAA Strategic Analysis

This section outlines the data transformation process required to transform raw datasets Passenger Traffic, Visitor Spending, Local Employment, and Tourism Visitation into a clean format using **Tableau Prep Builder**.

## 1. Monthly Screened Passenger Traffic
**Objective:** Convert "Wide" monthly reporting into a "Long" time-series format.

* **Pivoting:** Applied a *Columns-to-Rows* pivot to consolidate 80+ monthly columns into a single `Date` field and a corresponding `Passenger_Count` field.
* **Data Cleaning:** Removed non-numeric symbols (e.g., ".." representing missing pandemic data) and stripped punctuation to convert values into integers.
* **Strategic Filtering:** Filtered the "Screened Traffic" column to isolate **Transborder (U.S.)** and **Other International** sectors to focus on high-value recovery segments.

## 2. Visitor Spending (Statistics Canada)
**Objective:** Strip administrative quality flags and standardize quarterly timelines.

* **Fill Down:** Populated the `Area of Residence` and `Mode of Transport` columns, which contained null values in the raw CSV due to group-header formatting.
* **Quality Flag Removal:** Created a calculated field to strip Statistics Canada quality indicators (A, B, C, D, E) and provisional markers ("p") from numeric spending values.
* **Date Standardization:** Used the `DATEPARSE` function to transform quarterly strings (e.g., "Q1 2019") into standardized Date objects for timeline visualization.
* **Metric Isolation:** Filtered "Visit Statistics" to focus exclusively on **Expenditures per visit** to measure the economic efficiency of different traveler segments.

## 3. Halifax Employment Data
**Objective:** Map generic headers to years and clean category labels.

* **Header Reassignment:** Manually mapped and renamed generic field names (F3 through F9) to their respective years (2019–2025) to correct for header-alignment issues in the source file.
* **Footnote Stripping:** Used the "Remove Numbers" tool to strip numeric footnote suffixes from employment categories (e.g., "Private sector employees 8" became "Private sector employees").
* **Normalization:** Pivoted the annual columns into a vertical format, allowing for direct correlation with monthly airport traffic trends.

## 4. Tourism Nova Scotia Visitation
**Objective:** Isolate airport-specific arrival data and standardize market segments.

* **Mode Filtering:** Filtered "Mode of Entry" to keep only **Air** arrivals, ensuring the data reflects travelers impacting Halifax International Airport operations.
* **Temporal Filtering:** Restricted the dataset to a **2019–2025** window to match the baseline and recovery periods of the associated traffic and spending files.
* **Market Categorization:** Grouped detailed visitor origins into three primary strategic segments: **Domestic**, **US (Transborder)**, and **International (Overseas)** using conditional logic.

---

## Conclusion of Wrangling
By standardizing the **Date**, **Geography**, and **Numeric** formats across these four sources. This clean structure enables the analysis of the correlation between local economic recovery (Employment) and the specific high-value international travel segments (Spending and Visitation).
