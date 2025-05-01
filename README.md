## COHORT ANALYSIS USING PYTHON
![Intro_image](https://github.com/Temperance-Godwin/COHORT-ANALYSIS/blob/main/Intro.png)

## INTRODUCTION.
In the competitive landscape of online retail, understanding customer behavior is crucial for driving growth, increasing retention, and improving marketing strategies. Cohort analysis offers a powerful lens through which businesses can track and compare groups of customers (cohorts) based on shared characteristics—most commonly the time of their first purchase.

## OBJECTIVE
This project focuses on analyzing customer purchasing behavior over time by performing a cohort analysis using transactional data from an online retail store. The goal is to understand customer retention trends, identify churn patterns, and derive actionable insights to improve customer engagement and loyalty.

## DATA SOURCE
UCI Machine Learning Repository. View data [here](https://archive.ics.uci.edu/dataset/352/online+retail)

## LIBRARY USED
1. Pandas - Data Wrangling
2. Matplotlib - Data Visualization
3. Seaborn- Data Visualization

## METHODOLOGY
1. Data Loading & Cleaning
- Loaded data and removed missing CustomerIDs.
2. Cohort Mapping
- Assigned each customer to a CohortMonth.
- Calculated CohortIndex as the number of months since first purchase.
3. Retention Matrix
- Created a pivot table showing the number of retained customers over time per cohort.
- Normalized into percentages for clear retention visualization.
4. Visualization
- Generated a **heatmap** of monthly retention percentages using 'seaborn'.

View my code [here](https://github.com/Temperance-Godwin/COHORT-ANALYSIS/blob/main/Cohort%20Analysis.ipynb)

## INSIGHTS

1. There is a significant drop in retention after first purchase. Across nearly all cohorts, Month 0 (first purchase month) shows strong participation. However, in Month 1, there is a sharp drop—often greater than 50%, indicating that a large percentage of customers do not return after their initial transaction. This suggests that the business currently lacks a strong post-purchase engagement strategy or incentives to drive repeat purchases.

2. Most cohorts show a steep retention curve, where users quickly disengage after their first or second month. This implies a transactional business model with low customer loyalty, and highlights a missed opportunity in cultivating long-term relationships.

3. Certain monthly cohorts (e.g., those starting in November or December) demonstrate slightly higher Month 1 and Month 2 retention. This may correlate with holiday promotions, gift shopping behavior, or seasonal campaigns that resonate more strongly with customers.

4. Although few customers remain after Month 1, those who do return in Month 2 or 3 tend to remain active longer. This indicates a retention threshold — once customers pass through the early drop-off window, their likelihood of becoming loyal increases.

5. The heatmap visualization confirms that most cohorts have low retention rates across all months. This suggests the issue is systemic, not isolated to a single campaign, product, or season — and will require strategic, cross-functional intervention.

6. There is no visible indication of delayed spikes or growth in user counts in later months, which could indicate word-of-mouth or referral-based return traffic. This implies that customers are not actively referring others, and there's minimal network-driven growth.

## RECOMMENDATIONS
1. **Launch cohort-based retention campaigns based on a customer’s stage in their lifecycle (e.g., month 1, month 2, month 3) by:**
   
- Using marketing automation tools (e.g. HubSpot) to set up lifecycle email sequences.
- Creating triggers such as "7 days after first purchase" or "30 days of inactivity" to send personalized reminders, discounts, or product suggestions and includng dynamic content in emails based on past purchase history or categories browsed.

2. **Introduce a loyalty program to reward returning cutomers by:**

- Implementing a points-based system where customers earn rewards for each purchase, using custom-built solutions to integrate loyalty tracking and tracking performance by comparing retention rates pre- and post-loyalty program.

3. **Encourage the second purchase with first-time buyer offers by** including an offer inside the package delivery (e.g., a coupon code or QR to redeem bonus on next order).

4. **Identify and prioritize high-retention cohorts by:**

- Using the cohort heatmap to find months with above-average second or third-month retention.
- Looking into external factors during those periods (promotions, holidays, campaigns) and replicating effective tactics from high-performing months (e.g., offer bundles, timing of promotions).

5. **Monitor revenue retention, not just user count by:**
   
- Modifying the cohort analysis to track revenue (TotalSum) per cohort across months, normalize revenue by cohort size to calculate average revenue retained per user over time and using it to focus resources on cohorts that are both large and high-value.


## LIMITATIONS
While this analysis provides useful insights, there are several limitations to consider:
1. **Data is Limited to Few Continents**: Retention behavior may differ significantly in other markets due to cultural, economic, or seasonal factors.
2. **Temporal Range is Not Fully Defined**: The dataset likely covers a single year. A longer time horizon would provide a more complete view of long-term retention and customer lifetime value.
3. **Lack of Channel Attribution**: The dataset does not include information about how customers were acquired (e.g., paid ads, organic search, referrals). Without this, we cannot determine which marketing channels produce higher-retaining customers.
4. **Revenue Retention is Not Analyzed**: The focus was on user retention. Revenue retention would provide a more nuanced understanding of customer value and help distinguish between low- and high-spending retained users.
5.**No Behavioral or Demographic Segmentation**: All users are treated equally in the analysis. Further segmentation by age, gender, product type, or user behavior could uncover more granular insights.
6. **Returns and Cancellations Excluded but Not Analyzed**: While returns were excluded for data quality, analyzing their frequency and causes could reveal issues affecting customer satisfaction and long-term retention.


![Thank you](https://github.com/Temperance-Godwin/Forbes-world-billionaires-2022/assets/156975460/f6563ba6-1ad6-4d34-a3f3-8e7fbdf654df)

## Thank you for following through.

