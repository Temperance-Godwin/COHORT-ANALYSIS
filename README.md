## COHORT ANALYSIS USING PYTHON
![Intro_image](https://github.com/Temperance-Godwin/COHORT-ANALYSIS/blob/main/Intro.png)

## INTRODUCTION.
In the competitive landscape of online retail, understanding customer behavior is crucial for driving growth, increasing retention, and improving marketing strategies. Cohort analysis offers a powerful lens through which businesses can track and compare groups of customers (cohorts) based on shared characteristics—most commonly the time of their first purchase.

This project focuses on performing a cohort analysis of online retail customers, grouped by the month of their first transaction. The objective is to evaluate customer retention trends, repeat purchase behavior, and lifetime value over time. By analyzing how different cohorts behave after their initial interaction with the platform, we can uncover insights that inform customer engagement strategies, promotional timing, and product recommendations.

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
1. **Launch cohort-based retention campaigns based on a customer’s stage in their lifecycle (e.g., month 1, month 2, month 3).**
   
*How to Do It:*
- Use marketing automation tools (e.g. HubSpot) to set up lifecycle email sequences.
- Create triggers such as "7 days after first purchase" or "30 days of inactivity" to send personalized reminders, discounts, or product suggestions.
- Include dynamic content in emails based on past purchase history or categories browsed.

2. **Introduce a loyalty program to reward returning cutomers**

*How to Do It*:
- Implement a points-based system where customers earn rewards for each purchase.
- Use custom-built solutions to integrate loyalty tracking.
- Offer milestones such as “Get 10% off your third order” or “Earn a free gift on your fifth purchase.”
- Track performance by comparing retention rates pre- and post-loyalty program.

3. **Encourage the second purchase with first-time buyer offers**

*How to Do It:*
- After the first purchase, trigger a limited-time discount (e.g., 15% off if they return within 10 days).
- Include an offer inside the package delivery (e.g., a coupon code or QR to redeem bonus on next order).

4. **Identify and prioritize high-retention cohorts**
   
*How to Do It:*
- Use the cohort heatmap to find months with above-average second or third-month retention.
- Look into external factors during those periods (promotions, holidays, campaigns).
- Replicate effective tactics from high-performing months (e.g., offer bundles, timing of promotions).

5. **Segment customers by value for personalized treatment**:

*How to Do It*
- Use RFM (Recency, Frequency, Monetary) segmentation to classify customers.
- Send premium offers, early access, or VIP experiences to top-tier users.
- Send reactivation emails with low-cost offers or surveys to lower-tier or inactive users.

6. **Add product-based retention analysis by understanding which products or categories lead to higher customer retention.**
   
*How to Do It*:
- Segment your cohort analysis by top-selling product categories.
- Compare retention heatmaps across these categories to identify retention-driving products.
- Promote products that tend to generate returning customers more prominently on your homepage and ads.

7. **Monitor revenue retention, not just user count**
   
*How to Do It*:
- Modify the cohort analysis to track revenue (TotalSum) per cohort across months.
- Normalize revenue by cohort size to calculate average revenue retained per user over time.
- Use this to focus resources on cohorts that are both large and high-value.

8. **Automate retention tracking with dashboards**
   
*How to Do It*:
- Use tools like Power BI, Tableau, or Python Dash to build real-time retention dashboards.
- Schedule weekly or monthly data pulls and refreshes.
- Include visual alerts or trend indicators when certain cohorts fall below expected retention thresholds.

## LIMITATIONS
While this analysis provides useful insights, there are several limitations to consider:
1. **Data is Limited to a Single Geography**: The dataset only includes customers from the United Kingdom. Retention behavior may differ significantly in other markets due to cultural, economic, or seasonal factors.
2. **Temporal Range is Not Fully Defined**: The dataset likely covers a single year. A longer time horizon would provide a more complete view of long-term retention and customer lifetime value.
3. **Lack of Channel Attribution**: The dataset does not include information about how customers were acquired (e.g., paid ads, organic search, referrals). Without this, we cannot determine which marketing channels produce higher-retaining customers.
4. **Revenue Retention is Not Analyzed**: The focus was on user retention. Revenue retention would provide a more nuanced understanding of customer value and help distinguish between low- and high-spending retained users.
5.**No Behavioral or Demographic Segmentation**: All users are treated equally in the analysis. Further segmentation by age, gender, product type, or user behavior could uncover more granular insights.
6. **Returns and Cancellations Excluded but Not Analyzed**: While returns were excluded for data quality, analyzing their frequency and causes could reveal issues affecting customer satisfaction and long-term retention.
7. **No Real-Time or Automated Monitoring**: This is a static analysis. For production use, this should be built into a real-time dashboard or periodic reporting system to monitor cohort performance continuously.
