<div align="center">

# 📊 Healthcare Appointment No-Shows Analytics

### Understanding Why Patients Miss Medical Appointments — & How to Optimize Attendance

<!-- Technologies Badges -->
<p align="center">
  <img src="https://img.shields.io/badge/Microsoft_Excel-217346?style=for-badge&logo=microsoftexcel&logoColor=white" />
  <img src="https://img.shields.io/badge/Pivot_Tables-007ACC?style=for-badge" />
  <img src="https://img.shields.io/badge/Power_Query-F2C811?style=for-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Data_Visualization-12303A?style=for-badge" />
</p>

</div>

---

## 📌 Project Overview

Missed medical appointments lead to wasted clinical resources, increased waiting lists, and delayed patient care. This project provides an end-to-end data analytics study on **106,982 medical appointments** (Brazil dataset, April–June 2016).

The analysis covers data cleaning, custom feature engineering, multi-dimensional pivot tables, and an interactive **Healthcare No-Show Analytics Dashboard** in Excel.

---

## 📊 Key Performance Indicators (KPIs)

<div align="center">

| Total Appointments | Distinct Patients | Overall No-Show Rate | Average Wait Time | Total Clinics / Areas |
| :---: | :---: | :---: | :---: | :---: |
| **106,982** | **60,270** | **20.3%** | **10.17 Days** | **81 Neighbourhoods** |

</div>

> 💡 **Core Insight:** Approximately **1 in every 5 booked appointments** is missed (21,675 out of 106,982).

---

## 🧹 Data Cleaning & Preparation

1. **Filtering Invalid Data:** Removed 5 erroneous records where `Date.diff` was negative (appointments booked after the appointment date).
2. **Boolean Labeling:** Converted raw True/False flags into clear descriptive labels (`SMS received` / `SMS not received`, `has chronic` / `no chronic`).
3. **Feature Engineering (4 New Attributes):**
   - `Has_Not_Showed`: Numeric flag (`1` for missed, `0` for attended) enabling direct summation.
   - `Lead_Time_Group`: Categorized wait times (`Same day`, `1–3 days`, `4–7 days`, `8–14 days`, `15–30 days`, `More than a month`).
   - `Age_Group`: Segmented into life stages (`Kids: 1–12`, `Teenagers: 13–20`, `Adults: 21–40`, `Grand adults: 41–60`, `Elder people: 61+`).
   - `Has_Chronic`: Unified health condition indicator combining Hypertension and Diabetes flags.

---

## 💡 Key Business Findings

### 1️⃣ The Wait-Time Factor (Lead Time)
- **Same-day bookings** have an exceptionally low no-show rate of only **4.7%**.
- Waiting longer than **15 to 30 days** increases the no-show rate up to **32.7%–33.2%** (more than **7x higher**).

### 2️⃣ Demographics & Age Groups
- **Teenagers & Young Adults (13–20)** represent the highest flight-risk cohort with a **25.8%** no-show rate.
- **Elderly Patients (61+)** show the highest commitment with the lowest no-show rate at **15.2%**.
- Gender plays no significant role in attendance behavior (**20.4% Female** vs **20.1% Male**).

### 3️⃣ SMS Reminders Paradox
- Patients who received SMS reminders experienced a **27.7%** no-show rate versus **16.7%** for those who did not.
- *Analytical Nuance:* SMS reminders were predominantly assigned to long-lead appointments, which intrinsically suffer from higher absence rates.

### 4️⃣ Geographic Variances
- Highest no-show rates occur in **Santos Dumont (29.1%)**, **Itararé (26.3%)**, and **Jesus de Nazareth (24.9%)**.
- Lowest no-show rates belong to **Santa Martha (16.1%)** and **Jardim da Penha (16.3%)**.

---

## 📈 Dashboard Architecture

The interactive Excel dashboard (`Clean_Task8.xlsx`) is styled with a modern **Deep Maroon / Burgundy theme** and includes:

- **Executive KPI Cards:** Quick summary metrics for appointments, unique patients, SMS coverage, no-show rate, and average lead time.
- **Interactive Slicers:** Dynamic filtering by `Age_Group`, `Gender`, `Showed_up`, `Lead_Time_Group`, and `SMS_received`.
- **Integrated Visualizations:**
  1. *No-Shows by Age Group & Gender* (Horizontal Bar Chart)
  2. *No-Shows by SMS vs Chronic Conditions* (Breakdown Chart)
  3. *No-Shows by Waiting Days / Lead Time* (Column Chart)
  4. *Appointments vs. No-Shows by Neighbourhood* (Clustered Column Chart)

---

## 💡 Strategic Recommendations

- 📅 **Optimize Scheduling:** Encourage same-day or short-notice booking slots whenever feasible.
- 📞 **Targeted Follow-ups:** Implement direct confirmation calls for appointments scheduled more than 14 days in advance.
- 🔔 **Smarter Communication:** Re-align SMS notification logic to target younger age groups via preferred digital channels.
- 🏥 **Geographic Resource Allocation:** Address transportation or accessibility challenges in high-rate areas like *Santos Dumont* and *Itararé*.

---

## 📁 Workbook Structure
```
├── Clean_Task8.xlsx                # Primary Excel Workbook
│   ├── Rawdata1                    # Original raw dataset (106,987 rows)
│   ├── DataCleaned                 # Processed dataset with engineered columns
│   ├── Pivot Table                 # Calculation tables & interactive slicers
│   ├── Dashboard                   # Final interactive dashboard UI
│   └── Sheet6                      # Drill-through breakdown of missed appointments
├── healthcare_noshows.csv          # Source CSV dataset
└── README.md                       # Documentation
```
---

<div align="center">

Made with 📊 Excel + 💼 Healthcare Analytics

<br/>

<!-- Connect with me Section -->
<h3>📫 Connect with me</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/alaa-ramadan-" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="https://www.kaggle.com/alaaaymanramadan" target="_blank">
    <img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-badge&logo=Kaggle&logoColor=white" alt="Kaggle" />
  </a>
  <a href="https://github.com/Alaa-Ramadan-Elsaidy" target="_blank">
    <img src="https://img.shields.io/badge/GitHub-181717?style=for-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
</p>

</div>
