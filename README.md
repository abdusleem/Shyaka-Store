# 📊 Shyaka Marketing Dashboard - Power BI Project

![Dashboard Preview](D1-%20Overview.png)

## 📌 Project Overview

**Shyaka Marketing Dashboard** is a comprehensive Power BI analytics solution designed to track, analyze, and optimize digital advertising campaigns across multiple platforms (Snapchat, Instagram, TikTok, Google Ads) for a fashion retail brand.

---

## 📂 Project Details

| Category | Details |
|----------|---------|
| **Field** | Digital Marketing Analytics / E-commerce |
| **Industry** | Fashion & Retail |
| **Client** | Shyaka (Fashion Brand) |
| **Period** | January - September 2025 |
| **Budget** | 300,000 SAR |
| **Revenue Generated** | 1,328,429 SAR |
| **ROI** | 343% |

---

## 🎯 Project Objectives

1. **Track campaign performance** across 5 seasonal campaigns (New Year, Ramadan, Spring, Summer, Back to School)
2. **Measure ROI and ROAS** for each ad and platform
3. **Analyze audience engagement** (Impressions, Reach, CTR, Engagement Rate)
4. **Optimize ad spend** by identifying high-performing platforms and content types
5. **Provide actionable insights** for future marketing strategies

---

## 🧩 Tools & Technologies Used

- **Power BI Desktop** - Dashboard design and data visualization
- **DAX (Data Analysis Expressions)** - Advanced calculated measures
- **Power Query** - Data transformation and cleaning
- **Excel** - Initial data preparation
- **Markdown** - Documentation

---

## ⚙️ Data Model Architecture

The project uses a **Star Schema** with 5 main tables:
```
Campaign (Dimension Table)
    ├── Ads (Fact Table)
        ├── Engagement (Fact Table)
        ├── ROI (Fact Table)
        └── Audience (Fact Table)
```

**Relationships:**
- Campaign → Ads (1:Many via CampaignID)
- Ads → Engagement (1:1 via AdID)
- Ads → ROI (1:1 via AdID)
- Ads → Audience (1:1 via AdID)

---

## 📊 Key Metrics (DAX Measures)

### Financial Metrics
```dax
Total Spend = SUM(ROI[Spend_SAR])
Total Revenue = SUM(ROI[Revenue_SAR])
Net Profit = [Total Revenue] - [Total Spend]
Overall ROI % = ([Total Revenue] / [Total Spend] - 1) * 100
ROAS = [Total Revenue] / [Total Spend]
Profit Margin % = [Net Profit] / [Total Revenue] * 100
Average CPA = AVERAGE(ROI[CPA_SAR])
```

### Engagement Metrics
```dax
Total Impressions = SUM(Audience[Impressions])
Total Reach = SUM(Audience[Reach])
Avg CTR % = AVERAGE(Audience[CTR_%])
Engagement Rate % = AVERAGE(Engagement[Engagement_Rate_%])
Total Conversions = SUM(ROI[Conversions])
```

---

## 📈 Dashboard Pages

### 1️⃣ Marketing Dashboard Overview
- Revenue & Spend trends over time
- ROI by Platform (Pie Chart)
- Campaign Performance (Bar Chart)
- Top 10 ads by ROI (Table)
- Key KPIs: Spend, Revenue, ROI, Conversions

### 2️⃣ ROI & Performance Analysis
- Revenue vs Spend by Platform
- ROAS by Campaign
- CPA by Campaign (Bar Chart)
- Profit Margin Trend (Line Chart)
- Top 10 Profitable Ads (Detailed Table)

### 3️⃣ Audience & Engagement Analysis
- Campaign Revenue by Content Type (Treemap)
- Campaign Reach Over Time (Area Chart)
- Engagement Trend by Platform (Line + Column Chart)
- Top Performing Content (Table)
- KPIs: Total Impressions, Reach, Engagement %, CTR %

---

## 🔍 Key Insights

### 💡 Insight #1: TikTok Dominates ROI
- **TikTok** achieved the highest ROI contribution: **27.61%**
- Average CPA on TikTok: **21.50 SAR** (vs. 150 SAR on other platforms)
- Video content on TikTok achieved **7% engagement rate**

### 💰 Insight #2: Seasonal Campaigns Drive Revenue
- **Summer Sale** generated highest revenue: **~400K SAR**
- **New Year Collection** achieved exceptional ROAS: **6.0**
- Seasonal campaigns had **40% higher conversion rates**

### 🎬 Insight #3: Video > Static Images
- Video content achieved **2.5x higher engagement** than static images
- Instagram Reels achieved **9.62% engagement rate**
- Carousel ads on Snapchat balanced cost and engagement

### 📈 Insight #4: Profit Margin Improved Over Time
- Profit margin increased from **73%** (Jan) to **83%** (Aug-Sep)
- Improved targeting reduced **CPA by 35%**
- **Back to School** campaign achieved highest profit margin: **83.34%**

### 🌟 Insight #5: AD_011 - The Star Performer
- **AD_011** (TikTok Story) achieved **19,898% ROI**
- Spent only **87 SAR**, generated **17,309 SAR revenue**, **399 conversions**
- This ad went **viral** with massive organic reach

---

## 💡 Recommendations

### ✅ 1. Increase TikTok Investment
- Allocate **40% of budget** to TikTok (currently ~25%)
- Focus on short-form videos (15-30 seconds)
- Leverage trending audio and hashtags
- **Expected Impact:** +25-30% ROI increase

### ✅ 2. Double Down on Seasonal Campaigns
- Increase budget for **Summer Sale** & **Ramadan** to 100K+ each
- Launch early-bird campaigns 2 weeks before season
- Use retargeting for previous engaged users
- **Expected Impact:** +40% revenue in peak seasons

### ✅ 3. Replicate AD_011 Strategy
- Analyze elements of AD_011 success (content, timing, targeting, CTA)
- Run A/B tests with similar content on other platforms
- **Expected Impact:** Discover 2-3 viral ads per month

### ✅ 4. Reduce Traditional Google Ads Spend
- Cut Google Ads budget by **20%**, reallocate to social media
- Focus only on Google Shopping Ads (higher conversion)
- **Expected Impact:** Save 15K SAR monthly for reinvestment

### ✅ 5. Implement Real-Time Engagement Scoring
- Auto-pause low-performing ads after 48 hours
- Auto-boost high-performing ads with **1.5x budget**
- **Expected Impact:** Improve ROAS from 4.43 to 5.2+

---

## 🖼️ Dashboard Preview

| Overview | ROI Analysis | Engagement Analysis |
|----------|--------------|---------------------|
| ![Overview](D1-%20Overview.png) | ![ROI](D2-%20Performance.png) | ![Engagement](D3-%20Audience%20&%20Engagement.png) |

---

## 📁 Project Structure
 ┃  [📊 Shyaka](./Shyaka.pbix) → Power BI dashboard file  
 ┃  [📜 Data](./Data.xlsx) → Database 



---

## 🚀 Future Improvements

- [ ] Integrate real-time API data from ad platforms
- [ ] Add predictive analytics for future campaign performance
- [ ] Implement automated alerting system for low-performing ads
- [ ] Create mobile-responsive version for on-the-go monitoring
- [ ] Add customer lifetime value (CLV) analysis
- [ ] Develop recommendation engine for optimal ad placement

---

## 📞 Contact

**Created by:** AbdulRahman Sleem  
**LinkedIn:** [https://www.linkedin.com/in/abdulrahmansleem/]  


---

## 📄 License

This project is for portfolio demonstration purposes. Data has been anonymized and modified for privacy.

---

## ⭐ If you found this project helpful, please give it a star!
