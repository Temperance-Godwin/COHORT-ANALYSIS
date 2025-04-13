# COHORT ANALYSIS USING PYTHON
![Intro_image](https://github.com/Temperance-Godwin/COHORT-ANALYSIS/blob/main/Intro.png)

## INTRODUCTION.
In the competitive landscape of online retail, understanding customer behavior is crucial for driving growth, increasing retention, and improving marketing strategies. Cohort analysis offers a powerful lens through which businesses can track and compare groups of customers (cohorts) based on shared characteristics—most commonly the time of their first purchase.

This project focuses on performing a cohort analysis of online retail customers, grouped by the month of their first transaction. The objective is to evaluate customer retention trends, repeat purchase behavior, and lifetime value over time. By analyzing how different cohorts behave after their initial interaction with the platform, we can uncover insights that inform customer engagement strategies, promotional timing, and product recommendations.

## LIBRARY USED
1. Pandas - Data Wrangling
2. Matplotlib - Data Visualization
3. Seaborn- Data Visualization


## METHODOLOGY
1. Data Loading & Cleaning
- Loaded data and removed missing CustomerIDs.
2. Cohort Mappin
- Assigned each customer to a CohortMonth.
- Calculated CohortIndex as the number of months since first purchase.
3. Retention Matrix
- Created a pivot table showing the number of retained customers over time per cohort.
- Normalized into percentages for clear retention visualization.
4. Visualization
- Generated a **heatmap** of monthly retention percentages using 'seaborn'.

View my code [here](https://github.com/Temperance-Godwin/COHORT-ANALYSIS/blob/main/Cohort%20Analysis.ipynb)

## INSIGHTS
1. **High Drop-Off After First Purchase**: Most customers only make one purchase, with retention dropping sharply after the first month.
2. Some Months(e.g December) show better retention, this might potentially be due to as a results of promotion or holiday campaigns.
3. Over 60% of customers do not return after their initial purchase.

## RECOMMENDATIONS
- **Engage Early:** Launch automated email follow-ups during the first month post-purchase.
- **Loyalty Programs:** Encourage repeat purchases with discounts or point-based systems.
- **Behavioral Segmentation:** Use RFM analysis to identify and prioritize high-value segments.
- **Incentivize Second Purchase:** Offer discounts or time-sensitive deals to encourage a second transaction.
- **Measure Revenue Retention:** Extend analysis beyond user count to include monetary value.

## LIMITATIONS

- **Geographic Bias:** Only UK customers analyzed — The results may not generalize globally.
- **Lack of Channel Attribution:** There are no distinction between acquisition sources (ads, organic, etc.).
- **One-Time Snapshot:** Data is not continuously updated; real-time dashboards could enhance relevance.
- **No Revenue-Based Retention:** This data is focused on user count rather than total spend.
- **Limited Feature Engineering:** Product categories, user types, or channel data could provide deeper insights.
