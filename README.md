# Business Intelligence with SAS Viya: Car Sales & Customer Sentiment

A Business Intelligence case study built in **SAS Viya (SAS Visual Analytics and Visual Text Analytics)**. It combines structured car-sales data with unstructured customer opinions to support decision-making for **"Fars Royce"**, a fictional automotive company. Advanced Big Data Analytics course, individual project.

## Business questions

- Which brands and models drive the most sales and keep the highest resale value?
- How do price, fuel efficiency and performance relate to sales volume?
- How do customers feel about each car model (positive, neutral or negative)?
- How can sales analytics and opinion analytics together improve decisions?

## Analyses performed in SAS Viya

| Analysis | What it shows |
|---|---|
| **KPI dashboard** | Sales by manufacturer (Ford leads, followed by Dodge and Toyota), resale value by manufacturer, sales by model (word cloud) and sales by vehicle type |
| **Diagnostic analytics** | Fuel efficiency vs. sales: cars with a fuel efficiency of 20–30 sell the most |
| **Comparative analytics** | Horsepower vs. power-performance factor, resale value vs. price, and sales vs. price; lower-priced cars sell in higher volumes |
| **Path analysis** | Sankey diagram of transitions between vehicle types (Car → Passenger/SUV) |
| **Network analysis** | Models as nodes sized by sales and colored by price, with sentiment details per node |
| **Text & sentiment analytics** | Customer opinions classified as positive, neutral or negative per model |
| **Social media analysis** | How online customer opinion can feed BI decisions |

A midterm project for the same course also covered descriptive and diagnostic dashboards in **Power BI** and predictive/prescriptive analytics (linear regression) in SAS Viya.

## Dataset

`data/car_sales_sentiment.csv`: 157 car models based on the Kaggle *Car Sales* dataset, extended with a customer `opinion` text column and a dealer `Locations` column for text analytics.

| Column group | Columns |
|---|---|
| Identity | `Unique_ID`, `Manufacturer`, `Model`, `Vehicle_type`, `Latest_Launch`, `Locations` |
| Sales & value | `Sales_in_thousands`, `__year_resale_value`, `Price_in_thousands` |
| Specifications | `Engine_size`, `Horsepower`, `Wheelbase`, `Width`, `Length`, `Curb_weight`, `Fuel_capacity`, `Fuel_efficiency`, `Power_perf_factor` |
| Text | `opinion` (customer review used for sentiment analysis) |

Data preparation: missing values removed and decimal separators normalized so SAS could read numeric fields correctly.

## Note

The reports and dashboards were built in a hosted SAS Viya environment, so there is no exportable source code. This repository documents the analysis and contains the prepared dataset.

## Tech stack

SAS Viya · SAS Visual Analytics · SAS Visual Text Analytics · Power BI
