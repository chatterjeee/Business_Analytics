# Bike Share Dashboard
## Project Overview
The Bike Share Dashboard project is designed to provide key performance insights to support strategic decision-making for the Bike Share company. This dashboard will offer an in-depth analysis of various metrics, including revenue trends, rider demographics, and profit analysis, enabling the company to optimize its pricing strategy, manage operations more efficiently, and better serve its customers.

## Requirements
The following key metrics and features will be included in the dashboard:

## Hourly Revenue Analysis:
Visualize revenue generated on an hourly basis.
Profit and Revenue Trends:
Analyze trends over time, focusing on profitability and revenue growth.

## Seasonal Revenue:
Identify how different seasons impact revenue generation.
## Rider Demographics:
Understand the demographics of riders (age, gender, location, etc.).
## Design & Aesthetic Requirements
The dashboard will be designed using the company's brand colors for consistency.
It will feature a user-friendly, easy-to-navigate layout, ensuring that decision-makers can access important insights quickly.
## Data Source
Access to the Bike Share databases will be provided.
In the absence of an existing database, a new one will be created from scratch to house the necessary data for the analysis.
## Development Timeline
Preliminary Version: A preliminary version of the dashboard will be delivered as soon as possible (ASAP). An estimated timeline for the full version will be determined based on data availability and the scope of additional requirements.


# SQL Query
with cte as (
select * from bike_share_yr_0
union
select * from bike_share_yr_1)


select dteday,season,a.yr, weekday, hr, 
rider_type, riders, price,COGS, 
riders * price as revenue, 
riders * price - COGS*riders as profit
from cte as a 
left join cost_table as b
on a.yr=b.yr

# Dashboard

![image](https://github.com/user-attachments/assets/54444c45-576f-44bc-ae29-60eebf5c4ad4)

# Analysis 
## Pricing Recommendation
As part of the analysis, the following pricing recommendations are provided for the next year:

## Conservative Increase:
Considering last year's significant price rise, a more conservative increase of 10-15% is recommended to avoid negatively affecting demand.

A 10% increase would raise the price from $4.99 to approximately $5.49.
A 15% increase would raise the price to about $5.74.

## Recommended Strategy:
Market Analysis: Conduct further research to gauge customer satisfaction and analyze market trends.
Segmented Pricing: Implement differentiated pricing for casual vs. registered users based on their price sensitivity.
Monitor and Adjust: Closely monitor customer reactions to the price changes and be prepared to make adjustments.
