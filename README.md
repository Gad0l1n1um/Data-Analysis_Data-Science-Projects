Toman Bike Share Data Analysis Project
Our Data Analysis Workflow
Create a Database
Develop SQL Queries
Connect Power BI to DB
Build a Dashboard in Power BI
Answer the Analysis Question
Email Requests
Request for Development of Toman Bike Share Dashboard
Dear Data Analyst,

We need your expertise to develop a dashboard for "Toman Bike Share" that displays our key performance metrics for informed decision-making.

Requirements:
Hourly Revenue Analysis
Profit and Revenue Trends:
Seasonal Revenue
Rider Demographics
Design and Aesthetics:
Use our company colors and ensure the dashboard is easy to navigate.
Data Source:
Access to our database will be provided. If no database, please create one.
Deadline:
We need a preliminary version ASAP.
Please provide an estimated timeline for completion and a recommendation on raising prices next year.

Best Regards,

SQL Server Information
SQL Server Name: [Your SQL Server Name]
SQL Query Developed for Power BI Visualization
sql
Copy code
WITH cte AS (
    SELECT * FROM bike_share_yr_0
    UNION ALL
    SELECT * FROM bike_share_yr_1
)
SELECT 
    dteday,
    season,
    a.yr,
    weekday,
    hr,
    rider_type,
    riders,
    price,
    COGS,
    riders * price AS revenue,
    riders * price - COGS AS profit
FROM 
    cte a 
LEFT JOIN 
    cost_table b
ON 
    a.yr = b.yr;
Icons Used in Power BI
Go to Flaticon
Search for the required icon type
Download the selected icon
Go to Online PNG Tools
Import the downloaded icon
Change the color from black to white if necessary
Download the modified icon
In Power BI, go to "Insert" > "Image" and import the icons.
Recommendation for Raising Prices Next Year
Price Analysis:
Average price of 2022: $4.99
Average price of 2021: $3.99
Difference: $1.00
Price Increase Calculation:
Percentage Increase: $1.00 / $3.99 = 25%
Demand Analysis:
Patronage in 2022: 2,049,576 riders
Patronage in 2021: 1,243,103 riders
Difference: 806,473 riders
Percentage Increase: 806,473 / 1,243,103 = 65%
Price Elasticity:
Price Elasticity: 65% (Demand Increase) / 25% (Price Increase) = 2.6
Recommendations:
Conservative Increase: A 10-15% price increase to avoid a potential price ceiling.
A 10% increase would set the new price at around $5.49.
A 15% increase would set the new price at approximately $5.74.
Recommended Strategy:
Market Analysis: Conduct further research to understand customer satisfaction, competition, and the economic environment.
Segmented Pricing Strategy: Consider different pricing for casual vs. registered users.
Monitor and Adjust: Implement the new prices and adjust based on customer feedback and sales data.
Credits
Icons: Flaticon
Data Source and Tools: AbsentData
