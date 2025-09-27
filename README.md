# WEBSITE TRAFFIC ANALYSIS

📍 ## Project Overview 
This project analyzes website traffic data (website_wata.csv) using Excel for EDA and predictive analysis. The goal is to understand user engagement, bounce behavior, and conversion drivers, and to build a simple regression model for predicting conversion rates.


- Here is a preview if my Dashboard
<img width="1150" height="521" alt="Dashboard101" src="https://github.com/user-attachments/assets/779ff2e1-bb57-46b6-88a1-b7be6e61d288" />

## Objectives
- Perform descriptive analysis (summary statistics, pivot tables, charts).
- Explore bounce rate, session duration, and page views.
- Identify patterns between previous visits and conversion rates.
- Build a predictive regression model to quantify how user behaviors influence conversion.
- Visualize and interpret insights.

## Tools Used 
- Excel
  - Pivot Tables & Charts
  - Data Analysis ToolPak (Regression)
  - Conditional Formatting
  - GitHub (documentation and version control)

## Sources and Dataset ⭐
- Website_Wata [Download Here](https://www.kaggle.com/datasets/anthonytherrien/website-traffic)
- Source : [Kaggle](Kaggle.com/datasets)


## Skills Demonstrated 
  - Data Cleaning
  - Data Exploration
  - Exploratory Data Analysis (EDA)
  - Data Visualization
  - Inferiantial Statistics analysis
  - Predictive Model (Regresison)

## Analysis and Insights 📈
### Traffic Source Analysis  
- Bounce Rate by Source: Social and Paid traffic showed the highest bounce rates, while Referral traffic had the lowest.  
- Conversion by Source: Organic and Referral traffic performed strongly in conversion efficiency.  
- Engagement: Organic and referred users tended to spend more time per session but had mixed conversion results.  
- Users from Social and paid sources spent more time on page compared to users from other sources

### User behavior Analysis 
- Conversion rates increase as previous visits increase. Users are more likely to convert if they keep coming back to the website
- New users browse more pages than returning users, precisely, most users browse 6–10 pages before leaving.
- Only 1% of users are deep explorers of the website, viewing 11+ pages per session
    ![Pie Chart](images/pie chart.png)
  
<img width="355" height="305" alt="pie chart " src="https://github.com/user-attachments/assets/6399b868-cbd2-4084-ba01-7c8f86d2de22" />

### Session Duration vs Conversion
- Sessions >5 minutes accounted for 19% of traffic but drove disproportionately higher conversions.  
- Short sessions (<2 minutes) made up ~50% of all traffic, indicating drop-off issues.

<img width="519" height="306" alt="histogram " src="https://github.com/user-attachments/assets/291a4ff4-a6d9-4c78-a5ad-1a71d0a18a8c" />



## Distribution Analysis  
1. How many sessions lasted less than 2 minutes?**  
   - Formula: `=COUNTIF(SessionDurationRange,"<2")`  
   - Result: **1003 sessions (~50%)** ended in under 2 minutes.  

2. **What percentage of sessions lasted longer than 5 minutes?**  
   - Formula: `=COUNTIF(SessionDurationRange,">5") / COUNT(SessionDurationRange)`  
   - Result: **19% of sessions** lasted longer than 5 minutes.  

3. **Histogram of Session Duration**  
   - Most sessions are short (<2 minutes).  
   - A minority stay long (5–20 minutes).  
   - **Insight:** Initial engagement is weak, but once past the 2-minute threshold, engagement is strong.  

4. **Above/Below Average Sessions**  
   - Average Session Duration ≈ **3.02 minutes**.  
   - Used IF formula to flag sessions above vs below average.  

5. **Contribution of Top 20% Longest Sessions**  
   - Top 20% (400 sessions) contribute **54% of total session time**.  
   - Shows the importance of a small **power-user segment**.  

6. **Quartile Analysis (Q1–Q4)** 
   - Q1 = ```QUARTILE.INC(Web[Session Duration],1)``` =0.82 min → 25% of sessions end in <1 min.  
   - Q2 = ``` QUARTILE.INC(Web[Session Duration],2) = 1.99``` = 1.99 min → 50% end in <2 min.  
   - Q3 = ``` QUARTILE.INC(Web[Session Duration],3) = 4.19``` = 4.19 min → 75% end in <4 min.  
   - Q4 = ``` QUARTILE.INC(Web[Session Duration],4) = 20.29``` = 20.29 min → longest sessions.

   - **Insight:** Engagement is skewed — most leave early, a small fraction stay very long.
The company should use content and remarketing to shift more people from Q2 → Q3 → Q4. The analysis highlights a critical retention challenge; half of all sessions end in under two minutes, suggesting ineffective first impressions or mismatched targeting. Marketing should prioritize improving landing page clarity, speed, and relevance to reduce quick exits. Sales and campaign strategies should focus on nurturing the top quartile of highly engaged users, who spend 4–20 minutes per session and represent the most valuable segment. Retargeting and lookalike campaigns can help scale this engaged audience, while personalized offers can convert them into paying customers.

## Predictive Analysis (Regression Model)
 **Dependent Variable:** Conversion Rate  
 **Independent Variables:** Page Views, Session Duration, Bounce Rate, Time on Page, Previous Visits  

**Regression Results:**  
- R² = **0.12** → model explains ~12% of variation in conversion.  
- **Key Predictors:**  
  - 📈 **Page Views, Session Duration, Time on Page** → positive effects on conversion.  
  - 📉 **Bounce Rate** → negative effect on conversion.  
- **Interpretation:**  
  - More engaged users (longer sessions, more pages, deeper time on page) convert at higher rates.  
  - High bounce rates reduce conversion probability.

## 📊 Visualizations  
- **Traffic Source Comparison** (Bounce Rate & Conversion)   
- **Coefficient Bar Chart:** Regression predictors   
- **Histogram:** Session duration distribution
- **Pie Chart** Page Views Bins & engagement 
- **Report Dashboard**

## Key Learnings 📚
- Social and Paid sources had high bounce rates → need landing page optimization.
- Returning users are more engaged and more likely to convert.
- Engagement (page depth & session duration) is the strongest driver of conversion.
- A small group of power-users accounts for most of the engagement.
- Bounce rate is a critical negative predictor of conversion.










