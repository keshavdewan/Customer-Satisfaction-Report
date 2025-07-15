# Customer Satisfaction Report
Step into the role of a data analyst at OmniRetail, a U.S. retail chain selling electronics and smart home products through both online and physical stores. To improve customer satisfaction and retention, the company has collected feedback throughout 2024.

<img width="497" height="252" alt="Gemini_Generated_Image_cw1sb9cw1sb9cw1s" src="https://github.com/user-attachments/assets/c8d573f7-0517-45d9-9a4b-aa5dfc46468a" />

## Challenge 💪
This challenge is part of Onyx Data Challenge & ZoomCharts mini challenge for the month of July
We've been provided with a customer satisfaction dataset combining satisfaction scores, purchasing behavior, demographics, support history, and location data.
 
## Mission 
Our mission is to create an analytical report that identifies the key factors influencing customer satisfaction and loyalty across different regions, customer demographics, and support experiences.

***
## Dataset

-  The Dataset comprises of 120 rows and 12 Columns
-  The data was collected throughout the year 2024.
-  It is a combined dataset that includes information on satisfaction scores, purchasing behavior, demographics, support history, and location data.

| Column Name | Description |
|:---|:---|
| Customer_ID | Unique customer identifier (for internal use only)  |
| Group | Customer classification: A, B, or C • Group A: High-frequency shoppers • Group B: Moderate-frequency • Group C: New or low-frequency  |
| Satisfaction_Score | Customer’s rating of their experience (1 = very poor, 10 = excellent)  |
| Age and Gender | Demographic attributes  |
| Location | City and State (e.g., Austin.TX), with Latitude and Longitude for geographic mapping  |
| Purchase_History | Indicates if the customer has made purchases (Yes/No)  |
| Support_Contacted | Whether the customer interacted with support  |
| Loyalty_Level | OmniRetail’s internal rating: Low / Medium / High loyalty  |
| Satisfaction_Factor | The main reason influencing the satisfaction score (e.g., Price, Product Variety, Packaging) |



***
## Key Questions for Analyses ❓
1.	What are the main factors contributing to high vs. low satisfaction scores?
2.	Are certain customer segments (by age, gender, group) more loyal than others?
3.	Which locations (cities or states) report consistently high or low satisfaction scores?
4.	Does contacting customer support negatively impact satisfaction?
5.	How do factors like “Price” or “Product Variety” influence customer loyalty?
6.	Do repeat purchasers report higher satisfaction compared to one-time buyers?
7.	Are there regional clusters of highly loyal or dissatisfied customers based on location data?
8.	What is the relationship between loyalty level and satisfaction score?
9.	Do specific demographic groups favor certain satisfaction factors (e.g., Packaging vs. Price)?

***
## Methodolgy 💼
This dashboard was developed using Power BI to provide a clear and actionable view of customer satisfaction report. The process involved several key steps:

1. Data Transformation (in Power Query)
  -  Loaded the raw dataset and verified data types to ensure accuracy.
  -  Split the single `Location` column into separate `City` and `State` columns to enable more granular geographic analysis.
  -  Created a calculated `Age_Group` column and `Satisfaction_Groups` to segment customers into logical `age` bins and  `satisfaction_scores` for demographic reporting.
  -  Created `region` column by further dividing states to different region of the country namely:
       
| Column Name | Description |
|:---|:---|
| Midwest | Illinois |
| South | Texas |
| West | Arizona, California |
| Northeast | New York, Pennsylvania |

2. Data Modeling
  - Ensured all columns, including the newly created ones, were correctly formatted and ready for calculations.
  - Established a solid and efficient foundation for writing accurate DAX measures.

3. DAX for Analysis & Interactivity
  -  Developed fundamental KPI measures, such as total customer count and average satisfaction score.
  -  Used `CALCULATE` and `ALL` to build comparison metrics, allowing for analysis of a specific segment against the overall average.
  -  Implemented advanced dynamic subtitles for charts using ISINSCOPE and SWITCH, making the visuals context-aware as the user drills down.

***
## Dashboard Overview 👀
This is a single page dashboard answering various questions. There are two ways to interact in this dashboard either with slicers or using the drill down charts
<img width="1270" height="701" alt="image" src="https://github.com/user-attachments/assets/de2c3958-2147-45e5-9486-59753b5ca2bb" />

## Key Insights 📚
The analysis revealed several key findings:
- 📈 Top Satisfaction Drivers: 'Product Quality' & 'Packaging' are the clear winners, boosting satisfaction rates 41% and 31% above the average, respectively. This trend is largely driven by customers in the 25-34 and 55+ age groups.
- ⚠️ Drivers of Dissatisfaction: On the flip side, 'Price', 'Features', and 'Ease of Use' were the most common reasons cited for low satisfaction scores, pointing to clear areas for operational improvement.
- 👑 What Different Loyalty Tiers Value: The analysis showed a fascinating split. Highly loyal customers prioritize 'Brand Reputation' and 'Product Quality', while low-loyalty customers are most impacted by practical issues like 'Ease of Use' and 'Delivery Speed'.
- 🌎 Geographic Hotspots: The Western region (California & Arizona) has the highest customer base and shows strong loyalty trends, closely followed by Texas in the Southern region.
- 📞 The Support Interaction Effect: While contacting customer care didn't have a major overall impact on satisfaction scores, the data shows it noticeably impacted loyalty scores, especially in the Western & Southern regions.

  ## Recommendations ☑️
  -  Focus on Key Satisfaction Drivers & Address Weaknesses - Feature like'Product Quality' and 'Packaging' in marketing campaigns to reinforce brand value and justify pricing.
  -   Implement a Tiered Customer Engagement Strategy     
      -   For Low-Loyalty Customers: Focus on fixing the fundamentals to win their trust. Offer improved delivery options, simplify the online checkout process, and provide clear tutorials or support to improve ease of use.
      -   For High-Loyalty Customers: Launch a VIP or "Advocate" program that rewards repeat purchases and reinforces the brand reputation they value. Offer them exclusive previews, loyalty points, and special recognition.
  -  Overhaul the Customer Support Experience - Treat every support interaction as a critical opportunity to build, not break, loyalty. Implement post-interaction surveys to identify specific pain points in the support process. Invest in training for support staff to not only resolve issues efficiently but also to actively work on retaining the customer's confidence and business.
  -  Replicate Geographic Success - Conduct a deep-dive analysis into these high-performing regions. Identify what makes them successful—are there specific regional marketing campaigns, store-level policies, product assortments, or logistical advantages? Create a playbook based on these findings and pilot these strategies in lower-performing regions to see if they can be replicated.
 
## Key Challenges & Learnings:
My biggest challenge was translating a dataset that seemed simple at first into a powerful, single-page story. Leveraging ZoomCharts was key, as its advanced drill-down capabilities made it possible to explore the data granularly and get clear answers. Although, navigating the limitations of custom visuals, specifically when trying to implement DAX-driven dynamic subtitles (which even AI couldn't solve!)

## Key Features 🏁
I specifically used zoomcharts visuals for this report and was amazed to see its features like:
- Fluid Drill-Down Experience: Its main strength lies in its fluid drill-down capability, allowing users to explore multiple levels of hierarchical data within a single chart smoothly, often with just a click, without the entire report needing to reload.
- Advanced Cross-Chart Filtering: Drilling down on a ZoomCharts visual instantly filters all other charts on the report page. This creates a deeply interconnected and context-aware analytical experience.
- High Performance: The visuals are optimized for performance, ensuring that interactions like drilling down and filtering remain fast and responsive, even when working with large datasets.

***

## Conclusion
This analysis of OmniRetail's 2024 customer data provides a clear, data-driven roadmap for improvement. Key findings show that while factors like `Product Quality` drive satisfaction, fundamental issues such as `Price` and `Ease of Use` are primary sources of customer dissatisfaction. 
The path forward requires a targeted strategy that addresses these core weaknesses, overhauls the customer support experience to build loyalty, and engages different customer segments based on their unique needs. Acting on these insights will enable OmniRetail to boost customer retention and drive sustainable growth.

***
## Related Links
#### [Onyx Data Challenge July 2025](https://datadna.onyxdata.co.uk/challenges/july-2025-datadna-customer-satisfaction-and-loyalty-analytics-challenge/)
#### [ZoomChart Mini Challenge](https://zoomcharts.com/en/microsoft-power-bi-custom-visuals/challenges/onyx-data-july-2025)
#### [Medium Link](https://medium.com/@kdrokz/customer-satisfaction-report-0842b2d2607a)
#### [Power BI Dashboard](https://github.com/keshavdewan/Customer-Satisfaction-Report/blob/main/Customer%20Satisfaction%20Report.pbix)
