# 📊 Meta Ad Performance Analysis Dashboard

## 📌 Project Overview
This project presents an interactive **Power BI dashboard** to analyze Facebook and Instagram ad performance across the complete marketing funnel—from impressions to conversions. It provides a comprehensive view of campaign reach, engagement, conversions, and budget utilization to support data-driven decision-making.

---

## 🎯 Business Objective
- Track performance of ad campaigns across key KPIs  
- Identify the most effective platform (Facebook vs Instagram)  
- Analyze audience engagement and behavior patterns  
- Optimize budget allocation and improve ROI  

---

## 📂 Scope of Analysis

**In Scope:**
- Paid ad campaigns on Facebook and Instagram  

**Out of Scope:**
- Messenger and Audience Network  
- Organic engagement  

---

## 🛠️ Tools & Technologies
- **Power BI** (Dashboard & Visualization)  
- **DAX** (KPI calculations & dynamic measures)  
- **Excel** (Data preparation)  
- **Data Modeling (Star Schema)**  

---

## 🧩 Data Model

The dashboard follows a **Star Schema** for efficient analysis:

### 🔹 Fact Table
- `ad_events` → Stores all interaction events (Impressions, Clicks, Shares, Comments, Purchases)

### 🔹 Dimension Tables
- `ads` → Ad platform, ad type, targeting details  
- `campaigns` → Budget and campaign duration  
- `users` → Demographics (age, gender, country)  
- `date_table` → Time-based analysis  

---

## 📅 Calendar (Date) Table

A dedicated **Date Table** is created to support time-based analysis.

### Key Columns:
- Date  
- Year  
- Month & Month Name  
- Week Number  
- Day of Week  

### Purpose:
- Enable weekly and monthly trend analysis  
- Support calendar heatmap visualization  
- Improve filtering and relationships with `ad_events`  

---

## 🔄 Dynamic Measure (KPI Selector)

A **Dynamic Measure Table** is implemented to allow users to switch KPIs across visuals.

### Available KPIs:
- Impressions  
- Clicks  
- Engagements  
- Purchases  

### Sample DAX:
```DAX
Selected KPI = 
SWITCH(
    SELECTEDVALUE('Measure Table'[Metric]),
    "Impressions", [Impressions],
    "Clicks", [Clicks],
    "Purchases", [Purchases],
    "Engagements", [Engagements]
)
```

### Benefits:
- Interactive dashboard experience  
- Reduced visual duplication  
- Flexible analysis  

---

## 📊 Key KPIs & Definitions

| KPI             | Description                        |
|-----------------|----------------------------------|
| Impressions     | Number of times ads were displayed |
| Clicks          | Number of times users clicked ads |
| Shares          | Number of times ads were shared |
| Comments        | User comments on ads |
| Purchases       | Conversions generated |
| Engagements     | Clicks + Shares + Comments |
| CTR             | (Clicks ÷ Impressions) × 100 |
| Engagement Rate | (Engagements ÷ Impressions) × 100 |
| Conversion Rate | (Purchases ÷ Clicks) × 100 |
| Purchase Rate   | (Purchases ÷ Impressions) × 100 |
| Total Budget    | Total campaign spend |

---

## 📈 Dashboard Features
- **Gender Analysis** → Donut Chart  
- **Age Group Analysis** → Bar Chart  
- **Geographic Insights** → Map Visualization  
- **Monthly Trends** → Calendar Heatmap  
- **Weekly Trends** → Stacked Column Chart (by Ad Type)  
- **Hourly Trends** → Area Chart  
- **Ad Type Performance** → Matrix  

---

## 🔍 Key Insights
- High engagement (**CTR ~11.7%**) indicates strong ad creatives  
- Low purchase rate (~**0.6%**) shows drop-off in conversion funnel  
- Top audience: **Females aged 18–30**  
- Best-performing formats: **Video & Stories**  
- Peak engagement during **afternoon & evening hours**  
- High engagement regions: **India, US, Brazil**  

---

## 💡 Key Highlights
- Built an interactive KPI-driven dashboard using Power BI  
- Applied **star schema data modeling** for performance optimization  
- Performed **audience, geographic, and time-based analysis**  
- Implemented **dynamic KPI selection using DAX**  
- Identified funnel inefficiencies and improvement opportunities  

---

## 🚀 Recommendations
- Improve landing pages and conversion experience  
- Focus budget on **Video and Story ads**  
- Target **female audience aged 18–30**  
- Schedule ads during **peak engagement hours**  
- Allocate budget to **high-performing regions**  

---

## 📌 Conclusion
The dashboard highlights strong performance at the awareness and engagement stages but reveals a drop in conversions. By optimizing targeting strategies, ad creatives, and post-click experience, businesses can significantly improve campaign effectiveness and ROI.
