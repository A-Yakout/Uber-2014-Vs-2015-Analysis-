# 🚖 Uber NYC Data Analysis (2014 - 2015)

## 📌 Project Overview
This project is a comprehensive analysis of Uber's growth and user behavior changes in New York City between **April-September 2014** and **January-June 2015**. 

Using **Power BI**, I transformed millions of raw trip records into actionable business insights, revealing a massive Year-over-Year (YoY) growth and a strategic shift in usage patterns from "utility commuting" to "leisure & nightlife."

## 📂 Data Source
The dataset consists of over 18 million Uber pickups in NYC.
- **Source:** [Kaggle - Uber Pickups in New York City](https://www.kaggle.com/datasets/yakout11/uber-2014-and-2015)
- **2014 Data:** Contains specific Latitude/Longitude coordinates.
- **2015 Data:** Contains LocationIDs requiring mapping to a Taxi Zone Lookup table.

## 🛠️ Tech Stack
- **Tool:** Microsoft Power BI
- **Languages:** DAX (Data Analysis Expressions), Power Query (M)
- **Techniques:** Data Modeling, ETL, Geospatial Analysis, Time Intelligence

## ⚙️ Key Steps & Methodology

### 1. Data Cleaning & Transformation (ETL)
- **Standardization:** Unified column names across disparate 2014 and 2015 datasets.
- **Time Extraction:** Extracted attributes like `Hour`, `Day Name`, `Month`, and `Day Number` from timestamps to enable temporal analysis.
- **Geospatial Binning:** Rounded Latitude/Longitude coordinates in 2014 data to create "Hotspots" for map visualization.
- **Lookup Integration:** Merged 2015 data with a **Taxi Zone Lookup Table** to translate abstract Location IDs into real borough and zone names (e.g., "Manhattan", "JFK Airport").

### 2. Advanced Data Modeling
- **The "Bridge" Table:** Created a dynamic `MasterDate` table using DAX to bridge the two datasets.
- **Relationship Fix:** Engineered a `DateOnly` column in all tables to resolve granularity mismatches between timestamps and calendar dates, ensuring accurate relationships.
- **Custom Measures:**
  - Calculated **YoY Growth %** to quantify business expansion.
  - Developed **% Share of Week** measures to normalize data and visualize behavioral shifts independent of volume.

### 3. Dashboard Design
I designed 3 distinct dashboards to tell a complete story:

#### 📊 Dashboard 1: Temporal & Geospatial Dynamics (2014)
- **Focus:** Understanding the "Pulse" of the city.
- **Visuals:** Heatmap maps for hotspots, Line charts for daily peak hours (double peaks on weekdays vs. late-night peaks on weekends).

#### 🗺️ Dashboard 2: Zone Analysis (2015)
- **Focus:** Geographic distribution and demand clusters.
- **Visuals:** Matrix Heatmap (Day vs. Hour) highlighting the "Nightlife Economy", and Bar charts for Top 10 Pickup Zones.

#### 📈 Dashboard 3: YoY Market Evolution
- **Focus:** Strategic growth analysis.
- **Visuals:** Comparative Line Charts and KPI Cards showing the volume explosion and the shift in weekend vs. weekday market share.

## 💡 Key Insights
1.  **Explosive Growth:** Total trip volume grew by approximately **3x** Year-over-Year in the comparable months (April-June).
2.  **Behavioral Shift:** There was a marked increase in the percentage of **Weekend trips** in 2015 compared to 2014, indicating Uber's transition from a niche commuter tool to a mainstream leisure option.
3.  **The "Manhattan Core":** Despite expansion, over **90%** of trips remain concentrated in Manhattan and major airports, identifying Outer Boroughs (Queens/Brooklyn) as a massive untapped opportunity.

---
### 👤 Author
**Ahmed Yakout** Connect with me on LinkedIn: [linkedin.com/in/a-yakout](https://linkedin.com/in/a-yakout)
