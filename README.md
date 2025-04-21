# 🚖 Blu Cab Service Efficiency Analysis

## 📘 Project Overview

BlueCab Services offers cab rides from five airport pickup points across India. To enhance customer experience and operational efficiency, the company sought insights into how booking confirmations perform during **peak and non-peak hours** and the **impact of outliers** on booking outcome times. This project analyzes ride data and presents interactive visualizations in **Power BI**.

---

## 🗂️ Dataset Information

- [`CabRidersTable.csv`](https://github.com/rashi12121/Blu-Cab-Service-Efficiency-Analysis/blob/main/Blu%20Cab-Ride%20Data.csv) – Contains ride request details like timestamps, booking status, and outcome time  

---

## ❓ Business Questions

1. What is the **average booking efficiency** in each pickup area during peak vs. non-peak hours?
2. What are the **average cancellation time (ACT)**, **average booking time (ABT)**, and **average booking outcome time (ABOT)**?
3. What percentage of rides are **confirmed vs. unconfirmed**?
4. How do **outliers (Z-Score > 2)** impact booking outcome time?

---

## 📊 EDA & Visualization

### ✅ Task 1: ETL & Data Loading
- Imported CSV files into Power BI.
- Joined tables using Origin Area code.
- Classified rides based on **Peak Time**:
  - Morning Peak: 5:00 AM – 9:00 AM
  - Evening Peak: 6:00 PM – 11:00 PM
  - Others: Non-Peak

---

### ✅ Task 2: Efficiency Dashboard
Created a **dashboard** showing metrics for booking performance:
- **Total Rides**
- **Confirmed Rides** and **Confirmed Ride %**
- **Unconfirmed Rides** and **Unconfirmed Ride %**
- **ACT (Average Cancellation Time)**
- **ABT (Average Booking Time)**
- **ABOT (Average Booking Outcome Time)**

Filters:
- Time Category (Peak / Non-Peak)
- Pickup Area
![Overall Dashboard](https://github.com/rashi12121/Blu-Cab-Service-Efficiency-Analysis/blob/main/Blu%20Cab%20ABT_ACT.png)
---

### ✅ Task 3: Outlier Analysis
- Calculated **Z-Score** for Booking Outcome Time
- Binned Z-Scores into **0.20 intervals**
- Labeled Z-Scores:
  - `> 2` → **Outlier**
  - `≤ 2` → **Normal**
- Created visual breakdown of ride distribution across bins
![Outliers Dashboard](https://github.com/rashi12121/Blu-Cab-Service-Efficiency-Analysis/blob/main/Blue%20Cab%20Outliers.png)
---
### ⚖️ Task 4: Comparing Normal vs Outlier Data

Built an additional dashboard to:
- **Filter out outliers**
- Compare metrics only for “Normal” data
- Help visualize how outliers skew booking trends
![Outliers Impact Dashboard](https://github.com/rashi12121/Blu-Cab-Service-Efficiency-Analysis/blob/main/Blu%20Cab%20Outlier%20Impact.png)
---
## 📌 Key Insights

- **Filter by Area** shows that some zones underperform in confirmation rate during **evening peak**.
- **Average Booking Outcome Time** tends to increase during **non-peak hours**, possibly due to lower availability or system delays.
- Around **5–6% of rides** are categorized as **outliers**, which may distort overall service KPIs.
- Reducing these outliers could enhance service consistency and reliability.

---

## 🛠 Tools Used

- Power BI  
- DAX for calculated columns and measures – For ABT, ACT, ABOT, and Z-Score binning
- Power Query for data cleaning and transformation  
- CSV files


---


## 📈 Conclusion

The Power BI dashboard empowers BlueCab to:
- Make **data-driven decisions** during high-demand hours
- Identify and manage outliers that may skew performance metrics
- Prioritize efficiency improvements in critical pickup areas

This project sets the foundation for enhanced **ride booking reliability**, especially during peak periods.

