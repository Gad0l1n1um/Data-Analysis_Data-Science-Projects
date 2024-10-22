# Data Analysis Portfolio Project on Hotel Bookings

## Goal
Develop a database to analyze and visualize hotel booking data.

## Stakeholder Requirements
Build a visual data story or dashboard using Power BI to present to stakeholders, answering key business questions such as:

- **"Is our hotel revenue growing by year?"**

- **"Should we increase our parking lot size?"**

We aim to segment revenue by hotel type and understand trends related to guest behavior, such as whether they arrive with personal cars, which impacts parking lot usage.

## Objective
For each hotel, segment the revenue by hotel type to gain insights into key trends, including:

- Revenue growth over time.
- Guest behavior related to car ownership and parking lot needs.

## Tools Used
- **Excel**: For initial data handling and exploration.
- **MySQL**: For database management and querying.
- **Power BI**: For building visualizations and dashboards.

## SQL Code Used
The following SQL query was used to create a temporary table by joining multiple datasets to analyze hotel bookings:

```sql
CREATE TEMPORARY TABLE projects.all_years_joined AS
SELECT 
    a.*, 
    m.market_segment AS market_segment_name,
    c.meal AS meal_name,
    c.cost AS meal_cost
FROM 
    projects.all_years a
LEFT JOIN 
    projects.market_segment m
    ON a.market_segment = m.market_segment
LEFT JOIN 
    projects.meal_cost c
    ON a.meal = c.meal;

This query joins the hotel booking data (all_years) with the market segment and meal cost tables to provide a comprehensive view of bookings, including guest market segments and meal options.

## Recommendation

Based on the data analysis performed, here are the key recommendations for the hotel management:

Increase Parking Lot Size:

Our analysis shows that a significant portion of guests arrive with personal vehicles, indicating the need for additional parking space. Expanding the parking lot could improve guest satisfaction and accommodate future growth in car-owning guests.
Targeted Marketing for Different Market Segments:

Different market segments (e.g., business travelers vs. leisure travelers) show distinct booking patterns. The hotel should consider developing tailored marketing campaigns to attract more guests from high-revenue segments.
Monitor Meal Offerings and Costs:

The data on meal costs and preferences can help the hotel refine its food service offerings. Optimizing the menu based on popular choices and adjusting meal prices could boost profitability.
Seasonal Promotions:

Booking data reveals clear trends in occupancy rates during certain months or seasons. Offering special promotions or packages during off-peak times could help balance occupancy and maximize revenue year-round.

## Credits
Absent Data: For providing the dataset used in this analysis.