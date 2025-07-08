# ⚡ Energy Consumption and Cost Saving Dashboard (Tableau + Snowflake + AWS)

## 📘 Overview

This project analyzes household-level energy consumption (in KWH) and cost savings (in USD) across continents, countries, and energy sources. The goal is to uncover regional usage patterns and evaluate cost-saving potential using modern energy types like solar, wind, biomass, hydro and geothermal.

---

## 🧾 Dataset Summary

- **Rows**: 1,000  
- **Columns**: 12  
- **Features**:
  - Household ID  
  - Region (Continent)  
  - Country  
  - Energy Source  
  - Monthly Usage KWH  
  - Cost Saving USD  
  - Year  
  - Household Size  
  - Income Level  
  - Urban/Rural  
  - Adoption Year  
  - Subsidy Received

---

## ☁️ Cloud Architecture & Tools Used

This project demonstrates a realistic enterprise BI pipeline using modern cloud tools:

- **Amazon S3**: Raw dataset uploaded to S3 buckets  
- **AWS IAM**: Created a custom role (`tableau.role`) with trust policies for secure integration  
- **Snowflake**:
  - Loaded data from S3 using secure external stage
  - Created schemas and explored the dataset
  - Transformed the data using SQL (`UPDATE` + `SET`)
- **Tableau Desktop & Cloud**:
  - Connected Tableau Desktop to Snowflake
  - Designed the dashboard and published it to Tableau Cloud

---

## 📊 Dashboard Visuals

- Column charts for Monthly Usage KWH and Cost Savings by:
  - Continent
  - Energy Source  
- Bar charts for Monthly Usage KWH and Cost Savings by Country

---

## 🔍 Key Insights (from original dataset)

- 🌍 **Europe** shows the highest total energy consumption  
- 💰 **South America** leads in total cost savings  
- 🇳🇿 **New Zealand** has the highest KWH and cost savings for Solar and Geothermal  
- 🇦🇺 **Australia** leads in Biomass and Wind usage  
- 🇨🇳 **China** ranks lowest in Biomass energy use and cost savings

---

## 🧠 Skill Demonstration – Snowflake SQL

To showcase SQL transformation skills, custom logic was applied using `UPDATE` and `SET` statements:

- Increased `Monthly Usage KWH` based on `Income Level`:
  - Low → +10%  
  - Medium → +20%  
  - High → +30%
  
- Decreased `Cost Saving USD` using the same logic (inverse):
  - Low → -10%  
  - Medium → -20%  
  - High → -30%

These transformations were **not part of the original data** and were added to demonstrate backend manipulation in Snowflake.

---

## 🔐 Tableau Cloud Hosting

The dashboard is securely hosted on **Tableau Cloud**, connected directly to **Snowflake** with IAM-based access control.

Due to these enterprise-level integrations, the dashboard **cannot be made publicly accessible**.

---

## 🖼️ Dashboard Preview

![Dashboard Preview](Screenshots/Dashboard_Overview.png)

---

## ⚙️ Tech Stack

- Tableau Desktop & Tableau Cloud  
- Snowflake SQL  
- AWS S3 + IAM  
- SQL (`UPDATE`, `SET`, `CREATE`, `GROUP BY`)  
- Data modeling & ETL  
- Business Intelligence & Dashboarding

---

## 🚀 Project Status

✅ Data cleaned and loaded  
✅ Snowflake SQL transformations complete  
✅ Dashboard built and deployed  
📌 Portfolio-ready

